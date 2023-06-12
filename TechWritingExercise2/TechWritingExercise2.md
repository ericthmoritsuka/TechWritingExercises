449 words before

370 words now

With the end of benchmarking and optimization in 2010, we want to introduce a feature exclusive to the Enterprise Edition (EE) of the portal: the new Ehcache cluster replication mechanism.

Ehcache supports clustering and it uses the Remote Method Invocation (RMI) replication mechanism, which employs a point-to-point communication graph. However, this structure is not scalable for large clusters with numerous nodes as each node needs to send the same event to all nodes N-1 times. When the number of nodes (N) becomes too big, a significant network traffic problem appears.

Ehcache also creates a replication thread for each cache entity. In a large system like Liferay Portal, it is common to have more than 100 cache entities, resulting in 100+ cache replication threads which consume valuable resources like memory and CPU power. However, these threads spend most of their time idle, only activating when a cache entity needs to communicate with remote peers. So, ignore the heap memory used by these threads (as it depends on the application) and focus on the stack memory footprint of those threads.

Typically, the default thread stack size on most platforms is 2MB, which refers to 200+MB. Considering the heap memory size, this number may exceed 500MB (for one node!). Although memory is cheaper nowadays, we should not waste it. An abundance of threads can lead to frequent context switch overhead.

To address these issues, Liferay Portal uses ClusterLink, an abstract communication channel. The default implementation of ClusterLink utilizes JGroups' UDP multicast for communication. With ClusterLink, we can effectively resolve the problem of 1-to-N-1 network communication.

To reduce the number of replication threads, we introduce a small group of dispatching threads. These threads are dedicated to delivering cache cluster events to remote peers. Since all cache entities' cluster events pass through a single network point, we can use this to coalesce events. If two modifications to the same cache object occur close enough, we can notify remote peers once, saving network traffic.
 
(Newer versions of Ehcache support JGroups replicator, which can also address the 1-to-N-1 network communication issue, but they cannot fix the massive threads or perform coalescing.)

If you are interested in this feature, please contact our support engineers for more information.

<br>

[Go to TechWritingExercise1.md](../TechWritingExercise1/TechWritingExercise1.md)

[Go to TechWritingExercise3.md](../TechWritingExercise3/TechWritingExercise3.md)
