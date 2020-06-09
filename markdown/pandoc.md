I am designing this blog to make it as easy a possible for me to get
writing. I am trying to remove the little hurdles, so I can focus on
writing and not get blogged down in code, or endlessly tweak settings.

I started writing the blog in Markdown, which is easy enough to
understand, but still feels like writing code. I do most of my
development work in Visual Studio Code, which is an excellent editor and
is the best development environment on Windows in conjunction with
Windows Subsystem Linux. But one thing VS Code lacks (without using an
add-on) is a spell checker. With these two issues in mind, I started
looking for alternative ways I could setup my writing workflow.

I found there are a number of Markdown editors available and I
downloaded one to try. While it seemed to work fine, I didn’t want to
have to another piece of software installed on each of my computers. I’m
sure there are good Markdown editors out there, but I want to use the
tools I already have at my disposal. Whether this is the right approach
is hard to say; I’m testing what works for me.

I next checked if Microsoft Word can natively save to Markdown. It can
not. But a search revealed there is a good open source document
converter: [Pandoc](https://pandoc.org/index.html). Pandoc can convert a
huge number of document file formats, and is cross-platform. It has a
number of qualities I look for when evaluating software:

-   It’s open source, freely available

-   It’s been around a while, but is currently supported and has a good
    community

-   It has good documentation and examples

I did a quick install and test run. All seemed well. I wrote this
article in Word and used Pandoc to convert it to Markdown with the
following command:

    pandoc -s  website-architecture.docx -o website-architecture.md

My article workflow is now:

-   Write the blog post in Word (or Google Docs or Pages exporting to
    .docx when not on Windows)

-   Convert to Markdown with Pandoc

-   Generate a post with Hugo

-   Append the article Markdown to the Hugo post

-   Preview the post on the local Hugo server

-   Publish post by generating the static content with Hugo then pushing
    it to the GitHub repository

Well, that isn’t exactly the frictionless setup I was aiming for, but it
does have its benefits. I can write a blog post anywhere with Word or
another .docx compatible word processor. I can easily store all my posts
in Word, Markdown, and HTML; which all are useful in their own way. And
I found a new neat utility.

The downside is I will have to go through this lengthy conversion
process for every edit – no quick WYSIWYG fix. I will need to be careful
my post are well edited before leaving Word. I think I will be able to
tighten up the process a bit as well. I am aware that this is what I was
trying to avoid at the outset of this endeavour. The reliability and
extensibility of Pandoc to work with the conversions I throw at it is
another unknown factor.

Anyhow, it’s been interesting to figure out and time will tell how it
works.

Take care,

Conner
