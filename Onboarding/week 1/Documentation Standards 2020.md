[Documentation Standards](https://docs.google.com/document/d/1RxAwUhr4-JKpIEp1nriOL4GRctwCH3GQ7Ng998s4EHU/edit)

Documentation Standards 1
Formatting Standards 2
Line Breaks 2
Folder Names 2
Numbered Lists 2
Tables 2
Bold 2
Italics 3
Introducing Concepts 3
UI Elements 3
Terminology Standards 4
Exclusive Features 5
Phraseology Standards 5
Future Tense 5
Must 5
Dangling Participles 5
Subject/Object Agreement 5
Colons 6
Replace Wordy Clauses1 6
Editing Standards 9
Standards of Voice 9
Meta-Information 9
Cross Links 10
Definitions 10
Never Project Roles 10
Address the Reader with “You” 11
Software is Not in Control 11
Image Alt Text 11
Assume the Reader Has Read Nothing Else 11
Markdown Syntax Standards 12
Spaces / Tabs 12
Formatting Text 12
Aside / Admonition Syntax 12
Comparing Features 14
Images 14
Image Quality / Capture 15
Image Naming 15
Image Captions 15
Highlighting UI Elements 15
Article Naming 15
Videos 15
Action Items 17

There are several categories of standards:
Formatting Standards
Line Breaks
Single line; do not break at 80 columns. Separate paragraphs by using two carriage returns.
Folder Names
Because it’s a static site, folder names become part of the URL. For this reason, we must use appropriately named folders. The order of documentation is discernible inside the .rst files.
Numbered Lists
Single/double space; number all with 1. Multiple paragraphs must be indented to where the first paragraph starts.
Tables
| header 1 | header 2 | header 3 |
| --- | --- | --- |
| cell 1 | cell 2 | cell 3 |
Bold
Bold is used sparingly in the documentation. Why is this? Because too much bold is distracting. The reader's eye is drawn to bold text more than to anything else. All the headings are bold anyway, so we don't want to use it very much in the body text itself. There is one place where we want to use bold: field Lists.
When explaining a form that users can fill out, use bold for the field names.
Example:
Name: Enter the user's name.
Address: Enter the user's address.
Never end a section with a list of form elements, like I was about to do before I typed this sentence.
Italics
Below are some guidelines for when to use italics.
Introducing Concepts
If you're introducing a concept, italicize the concept the first time you use it. Thereafter, you don't need the italics.
Example: One of the primary ways of extending the functionality of Liferay Portal is by the use of plugins. Plugins are an umbrella term for installable portlet, theme, layout template, and web module Java EE .war files. Though Liferay comes bundled with a number of functional portlets, themes, layout templates, and web modules, plugins provide a means of extending Liferay to be able to do almost anything.
Notice the italics on plugins, portlet, theme, layout template, and web module the first time the terms are used, but none when the terms are used after they are introduced.
UI Elements
When you're telling the user to click on something in the UI, italicize it.
Example: Click the Save button to continue.
If you're referring to a UI element, but there's no direction for the user, capitalize it, but don't italicize it.
Example: After clicking the button, the Configuration page appears.
To provide as much clarity on UI elements as possible, let's combine the above two rules:
Example: On the Configuration page, click the Add button.
As you can see, the UI element that contains direction for the user is italicized, but the UI element that has no direction is not.
Terminology Standards
Developers tend to mangle even their own terminology. As a documentation team, we must fix these. If you see terminology in a document and you or your spell checker are in doubt, please look it up.

Examples:

Wrong
Right
backend
back-end
frontend
front-end
Javascript (or JS or js)
JavaScript
ServiceBuilder
Service Builder
RESTBuilder
REST Builder
openapi
OpenAPI
reindex
re-index
[LIFERAY_HOME]
[Liferay Home]
Out of the box
out-of-the-box

We also must have standards for our own terminology. Liferay uses terminology that’s fairly common to refer to Liferay-centric concepts. To differentiate the general use of these terms from the Liferay-specific use, we capitalize these terms when we refer to the Liferay-specific variant.

Examples:

Site
Generic: Liferay provides some great tools for designing your site.
Specific: To create a Site, click Sites -> New Site.
Organization
Generic: Liferay DXP is flexible enough to be a good fit for any organization.
Specific: Liferay Organizations can model the hierarchical structure of any real-world organization.
Role
User
Team
User Group
Exclusive Features

> Subscribers - Notes the feature is exclusive to enterprise subscribers. There is a badge system in progress to handle this.
> Phraseology Standards
> The Strunk and White (Elements of Style) Rule 13 states Omit Needless Words. This principle underlies our approach to phraseology.

Examples:
Future Tense
This action will create a new record in the database.
This sentence uses the future tense when there’s no need to use the future tense. Make it a goal to remove the future tense from all your Liferay writing. Instead, use the present tense:

This action creates a new record in the database.
Must
To use Assets, you need to have an Asset Renderer and an Asset Renderer Factory.
One word is better than two, and since “need to” is two words and “must” is only one, change this to must in all cases.
To use Assets, you must have an Asset Renderer and an Asset Renderer Factory.

Dangling Participles
Please do the following:
This is a “dangling participle,” because there’s no object following the following. Instead, use phrases like this:
Follow these steps:
Do these things:

Subject/Object Agreement
When a user performs this function, they get feedback.
“User” is singular; “they” is plural. In English, this is incorrect, though it’s becoming more common. There’s an easy way to resolve this in most cases: make the whole thing plural:
When users perform this function, they get feedback.
Other solutions to this problem are to alternate the singular form between the male and female pronouns:
When a user performs this function, she gets feedback.
When a user performs this function, he gets feedback.
Colons
Proper use of colons dictates they be placed only where you could place a period. That’s right: you must have a complete, independent clause to use a colon correctly. This means these usages are all wrong:

To use an accelerator:
To create a Site:
For example:

In the above examples, you’d use a comma instead of a colon.
Replace Wordy Clauses1
Here’s a list of common wordy clauses people use, and their shorter replacements. Again, this is an attempt to apply Rule 13 (Omit Needless Words).
whether or not = use whether by itself. You only need or not if you mean “regardless of whether”
in actual fact = remove or use actually
at the time that; at the time when = when
in the affirmative; in the negative = yes and no
at the present time; at this time; at present = now, today, currently
due to the fact that = because
inasmuch as = because or since
in excess of = more than or over
in regard to = about, regarding, concerning
literally = means actually; only use as an intensifier
presently = now or soon
previous to = before
prior to = before or until
question whether; question of whether; question as to whether = use the first
in the process of = remove
subsequently = later
subsequent to = after
simply = remove
just = remove
take a look = look
basic; basically; general; generally = remove
allow you to = lets you
directs you to = shows you
have the option of = can
a majority of = most
a number of = many
accounted for by the fact that = because
as a consequence of = because
due to the fact that = because
in view of the fact that = because
for the reason that = because
on account of = because
on the basis of = because
on the grounds that = because
owing to the fact that = because
an order of magnitude = ten times
are of the same opinion = agree
by means of = by, with
despite the fact that = although
during the course of = during, while
fewer in number = fewer
for the purpose of = for
has the capability of = can
having regard to = about
if conditions are such that = if
in all cases = always; invariably
in close proximity to = near
in connection with = about, concerning
in order to = to
in the event that = if
it is clear that = clearly
it is often the case that = often
it is worth pointing out that = note that
it may, however, be noted that = but
lacked the ability to = could not
large numbers of = many
prior to = before
inside of = in
you’ll need to = you must
allows you to = lets you
1https://www.extension.harvard.edu/inside-extension/cut-clutter-17-phrases-omit-your-writing-today and http://www.academicpeds.org/espauthoring/page_05.htm
Editing Standards
Use the text editor that works best for you. Various members of the team use these editors (in alphabetical order):

Atom
Neovim/Vim
Sublime Text
Textmate
Visual Studio Code

Make sure your editor can perform these functions:

Syntax highlighting, not only of Markdown, but also of the various programming languages used by Liferay (Java, JavaScript, Freemarker, Groovy/Gradle, XML, JSON, etc.).
Automatic spell check. If a word is highlighted automatically by your spell checker, you’re more likely to catch the error
Dynamic word wrapping. You must be able to turn this off to format tables and then turn it back on to go back to paragraphs.

If you are new and unsure of which editor to use, see anybody: the whole team loves to evangelize their particular editor.
Standards of Voice
What would BChan say (WWBCS)
Lunar Resort? If not, then we need a new example.

Meta-Information
We never talk about meta-information. For example, never say things like this:

This article is intended to…
This series of tutorials walks you…
At Liferay, we…

This is all filler and unnecessary. Keep pronouns strictly to you and don’t talk about reading articles or their format. I (Rich) have spent countless hours trying to excise this from the older docs, so I really don’t want to see it in the new docs.
Cross Links
When linking from one article to another, keep in mind that we avoid meta information (see above), even in links. For example, this is a bad link:

For more information see this article.

This is a good link:

For more information, see Friendly URLs.
Definitions
Definitions are paragraphs, with the item to be defined appearing in bold along with the colon. They should never be bulleted. Here are two example definitions:

Definition: A statement that describes the meaning of a term.

Term: An object, usually a noun, whose meaning must be defined.

Definitions must never use the term they’re defining in the definition.
Never Project Roles
Organizations are different. Workflows are different. Roles are different. Never project a role onto your reader when “you” should suffice. For example, never do this:

Administrators can create the directory...
Marketers can use Fragments....
Developers should create a class…

Instead, do this:

Create the folder…
You can use Fragments…
Create a class…

Note that you also Omit Needless Words by doing this.
Address the Reader with “You”
In training, it’s okay to say “we” are working on a particular topic, because there’s a teacher and everybody is learning together. In documentation, don’t address the reader with “we.” Be consistent and always use “you.”

Similarly, don’t say “let’s [do something].”
Software is Not in Control
Never word things in a way where the software is making the decisions or seems to be in control of the user. Always empower the user. For example, never say this:

This feature lets you…
A dialog pops up that allows you to…

Instead, put the user in control, not the software:

You can…
Use the dialog to configure…
Image Alt Text
Every image should have alt text, and it should be at least one descriptive, complete sentence. In other words, alt text comprised of simple labels isn't enough. DON'T do this for alt text:

The Liferay setup wizard.

Instead, do this:

The Liferay setup wizard makes connecting to your database and configuring a default administrator easy.
Assume the Reader Has Read Nothing Else
Each article should be as standalone as possible. Never assume the reader has (or might have) read another article on the same topic. If it’s helpful to link to another article, definitely do it, but avoid language like this:

You may have noticed this thing when [doing this other thing in this other article]. Here’s how it works.

Instead, do this:

At the bottom of the [form](link) is this other function. Here’s how to use it.

Markdown Syntax Standards
Spaces / Tabs
Hyperlinks - in-line w/ text - no need to be on separate line
Formatting Text
Bold
Italics
Aside / Admonition Syntax

```eval_rst
.. error::
   This is an error admonition using the `eval_rst` codeblock style.
```

```{error}error::
   This is an error admonition again using the shorthand codeblock.


* Here is a bullet item.   - Please note the spacing (3 spaces).
* An admonition   - It does not take a title argument.
* Here is an inline `code` example.
```

```{important}important::
   This is an important admonition.
```

```{note}note::
   This is a note admonition.
```

```{tip}tip::
   This is a tip admonition.
```

```{warning}warning::
   This is a warning admonition.
```

You can use code in line within an admonition:

`code`
One known issue is that you cannot use code blocks or code in-line within an admonition:

`code`

Or

```
  code
```

Comparing Features
When comparing features between items, such as Public and Private Pages, use a table with checks for the corresponding behavior:

| Behavior                                   | Public Pages | Private Pages |
| ------------------------------------------ | ------------ | ------------- |
| Visible to unauthenticated users           | &#10004;     |               |
| Viewing requires Login and Site Membership |              | &#10004;      |
| Distinct URL pattern                       | &#10004;     | &#10004;      |

Images
There is a shared images folder in the root of each documentation section. Place any image (such as images for icons; an image of the Control Panel, etc.) that is shared across the documentation here.

Use one of these prefixes as a naming convention:

icon-
button-
menu-

Image Quality / Capture
Image Naming
Images should be named as sequential numbers (01.png, 02.png), etc. Later we will review the cognitive debt this creates.
Image Captions
Image captions were a part of the old documentation standard. They required a custom extension to the Markdown parser that copied the alt text into a caption below the image. For the new docs, for speed purposes, we will use the same standard we had for captions for alt text with the exception of numbered figures. Alt text should be written as at least one complete sentence describing what’s going on in the image for the benefit of the vision impaired using screen readers.

Note: Do not add formatting (bold/italics) to alt text for images in your articles. It will break the build. :(
Highlighting UI Elements
Highlight / box select at most three elements. More than 3 makes it confusing to know what to focus on. Ideally a single element is highlighted.
Article Naming
Videos
Working with Multiple Software Versions
Contrary to the content distribution in Liferay Help Center, Liferay Learn does not include different articles for different minor software versions. The same Markdown file describes the same major software version (for example, version 7) with all the updates in minor software version (for example, 7.3, 7.4, and so on.)

When updating a Liferay Learn topic in the same minor version, as part of new product functionalities or content migration, consider the following information:
Do not create a new article to discuss the changes in a new software minor version. Keep all the content for the same software major version in the same article.
Place the newest information at the top of the article, and the oldest information at the bottom.
Evaluate the impact of the changes in the existing document:
For minor changes, use notes to let users know what product minor version the content applies to. Markdown example: > Available: Liferay 7.3+. If the change requires a header, place the note right after the header.
For major changes, use a dedicated H2 section to discuss the changes and place a note-type admonition at the beginning of the topic cross-linking the H2 (see Markdown Examples.)
Markdown Examples
Example 1 — You need to update a product feature discussed in software version 7.2. This feature incorporates a new functionality in 7.3, but the rest of the feature works in the same way it works in 7.2. In this case, use notes to signify the changes for the affected version:

# Organizing Content with Categories and Tags

    ## Vocabularies

[content for 7.2 and 7.3+ versions goes here]

    ### Vocabulary Visibility

    > Available: Liferay 7.3+.
    [content specific for 7.3 goes here]

Example 2 — Consider now the case where you must update content that changes significantly between the existing 7.2 and the new 7.3 version. In this case, write the content for the most recent version at the top, and use an H2 to place the previous content:

# About Collections and Collection Pages

```note::
This information applies to Liferay DXP 7.3+. For previous Liferay DXP versions, see `Liferay DXP 7.2 <#liferay-dxp-7.2>`_.
```

[content for 7.3+ version goes here]

## Liferay DXP 7.2

[content for 7.2 version goes here]

Formatting the Previous Content

If you need to copy content from Help Center into Learn or add new content in the same topic, consider the following information:

Newer versions go at the top of the Markdown file, older versions at the bottom.
Copy the content from the source Markdown file; do not use the source HTML file.
Create a new H2 for the content you're porting or updating at the end of the Markdown file. This H2 uses the name of the Liferay version the content applies to (for example ## Liferay 7.2.)
Update the header levels for the content you port or update. Because you are using an H2 to group this content, all previous H2 should change to H3, all H3 should change to H4, and so on.
Format of the content you paste. When copying and pasting content, you may find unexpected line endings or additional spaces between words or paragraphs.
If porting content from Help Center:
Remove any formatting options from the alt text in images. In Help Center, alt text contains formatting options like bold or italics. This is not supported in Learn and will cause your local Liferay Learn build to fail with an error similar to img_node['alt'] = ''.join(content).
Copy all the screenshots from the Help Center folder into the corresponding images folder in Learn. Rename the screenshots to use the Learn naming convention (01.png, 02.png, and so on.)
Update all the image links in the Markdown content you're porting, so images display correctly.
Always create the local Liferay Learn build and ensure that the content you're porting or updating renders as expected.

Action Items
Appendix A: Atom editor settings
Here are some suggested settings for editing articles and code.
Whitespace
If you use a Whitespace package, disable removal of trailing spaces for Markdown. You can do that with a config.cson file entry (Edit > Config…) like this:

".gfm.source":
whitespace:
removeTrailingWhitespace: false
editor:
showInvisibles: true

Setting showInvisibles: true helps to call out unwanted whitespace.

Editor Settings
You can set these for all scopes “\*” or as overrides in the Markdown scope “.gfm.source” to soft wrap lines in your editor, convert tabs to 4 spaces, and disable skipping over tabs with your cursor.

“\*”
editor:
atomicSoftTabs: false
softWrap: true
tabLength: 4
