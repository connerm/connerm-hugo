---
title: "Writing with Word and Pandoc"
date: 2020-06-04T20:08:28-07:00
draft: true
---
I am designing this blog to make it as easy a possible for me to get
writing. I am trying to get all the little hurdles out of the way so I
can focus on writing and not getting blogged down in code, or endlessly
tweaking settings.

I started writing the blog in Markdown, which is easy enough to
understand, but still feels like writing code than writing prose, at
least to me. And these days I do most of my development work in Visual
Studio Code. It’s an excellent editor and is the best development
environment on Windows in conjunction with Windows Subsystem Linux. But
one thing VS Code lack (without using an add-on) is a spell checker.
With these two issues in mind, I started looking for alternative ways I
could setup my writing workflow.

I found there are a number of Markdown editors available and I
downloaded one to try. While it seemed to work fine, I didn’t want to
have to another piece of software installed on each of my computers. I’m
sure there are good Markdown editors out there, but I felt like I wanted
to use the tools I already had at my disposal. Whether this is the right
approach it impossible to answer; I’m just doing what works for me.

I then tried to see if Microsoft Word could natively save to Markdown.
It could not. But a search revealed that there is a good open source
document convert: [Pandoc](https://pandoc.org/index.html). Pandoc can
convert a huge number of document file formats, and is cross-platform.
It has a number of things I look for when evaluating software:

-   It’s open source, freely available

-   It’s been around a while, but is currently supported and has a good
    community

-   It has good documentation and examples

I did a quick sudo apt install pandoc and did a test run. All seemed
well. I wrote this article, and the previous, in Word and used Pandoc to
convert them to markdown with:

    pandoc -s  website-architecture.docx -o website-architecture.md

My article workflow is now:

-   Write blog in Word (potential Google Docs or Pages exporting to
    .docx when not on Windows)

-   Convert to Markdown with Pandoc

-   Generate a post with hugo new …

-   Append article Markdown to the hugo post: cat
    ../blog-markdown/website-architecture.md &gt;&gt;
    context/posts/website-architecture.md

-   Preview the post on local hugo server

-   Publish post by generating the static content with hugo then pushing
    it to the github repository

Well, that isn’t exactly the frictionless setup I was aiming for… but
this does have it’s benefits. I can write a blog post anywhere with Word
or another .docx compatible word processor. I can easily store all my
posts in word, markdown, and html; which all are useful in their own
way. And I found a new neat utility.

The downside is that I will have to go through this lengthy conversion
process for every edit that gets noticed on the website – no quick
WYSIWYG fix. So I will need to be careful post are pretty well done this
step. I think I will be able to tighten up the process a bit, but I am
aware that’s what I was trying to avoid at the outset of this endeavour.
The reliability and extensibility of Pandoc to work with the conversions
I throw at are is another unknown factor.

Anyhow, it’s been interesting to figure this out and time will tell if
it works out.

Take care,

Conner
