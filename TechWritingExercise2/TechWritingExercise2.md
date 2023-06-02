449 words before

414 words now

As we approach the end of benchmarking and optimization in 2010, let's reflect on our recent activities. Today, we'll discuss a feature exclusive to the Enterprise Edition (EE) of the portal: the new Ehcache cluster replication mechanism.

Ehcache supports clustering, and by default, it utilizes the Remote Method Invocation (RMI) replication mechanism, which employs a point-to-point communication graph. However, this type of structure is not scalable for large clusters with numerous nodes as each node needs to send the same event to all other nodes N-1 times. When the number of nodes (N) becomes too big, a significant network traffic problem appears.

Ehcache also creates a replication thread for each cache entity. In a large system like Liferay Portal, it is quite common to have more than 100 cache entities, resulting in 100+ cache replication threads. Threads consume valuable resources such as memory and CPU power. However, these threads spend most of their time idle, as they only become active when a cache entity needs to communicate with remote peers. So, let's ignore the heap memory used by these threads (as it depends on the application) and focus on the stack memory footprint of over 100 threads.

Typically, the default thread stack size on most platforms is 2MB, which refers to 200+MB. When considering the heap memory size, this number may even exceed 500MB (for a single node!). Although memory is relatively cheaper nowadays, we should not waste it. An abundance of threads can lead to frequent context switch overhead.

To address both these issues, Liferay Portal offers a solution called ClusterLink, which is an abstract communication channel. The default implementation of ClusterLink utilizes JGroups' UDP multicast for communication. With ClusterLink, we can effectively resolve the problem of 1-to-N-1 network communication.

To reduce the number of replication threads, we introduce a small group of dispatching threads. These threads are dedicated to delivering cache cluster events to remote peers. Since all cache entities' cluster events pass through a single network point, we can take advantage of this to coalesce events. If two modifications to the same cache object occur close enough, we only need to notify remote peers once, resulting in saved network traffic.
 
(Newer versions of Ehcache support JGroups replicator, which can also address the 1-to-N-1 network communication issue, but it cannot fix the problem of massive threads or perform coalescing.)

If you are an EE customer interested in this feature, please feel free to contact our support engineers for more detailed information.

<br>

[Go to TechWritingExercise1.md](../TechWritingExercise1/TechWritingExercise1.md)

[Go to TechWritingExercise3.md](../TechWritingExercise3/TechWritingExercise3.md)