+++
title = 'Hello World'
date = 2025-10-13T14:08:56-04:00
+++

# Why?
I've been working on some things for a while, and realized that I can, or perhaps *should*, document it. Not only for myself, but that others might find it helpful too.

## Some things
Ok, I realize that 'some things' might be vague, but it is what it is.

Lately, I've been working on setting up some networking infrastructure at-home to allow me to have better control over what is on my network. At its core, you might call it paranoia--and that might not be entirely wrong--but I see many things becoming dependent on external services and infrastructure, and ultimately at the whims of those external services. Not only that, but connected devices often need to connect to a home server, when that shouldn't be necessary--although perhaps at the cost of more involved configuration. To that end, I want to have the ability to isolate the deivces I (mostly) trust and those over which I have no trust. 

This led me down a rabbit hole of things that I learned in high school, but haven't had the ability to do much about lately. So, I wanted to get back up to speed, and learn a bit more about it. With that said, I've kind of settled on an architecture for my home network, and that may help you understand what I am/was trying to do.

- Multiple VLANs, with seperate VLANs by device type, trust level, and roles.
- Self-hosted services, with as much running on Kubernetes as possible.
- Self-hosted storage; for now a Synology NAS, but eventually more redundant and resilient storage.
- Self-hosted time server; No particular reason but my most recent endeavor. GPS-derived and GPS-disciplined oscillator that provides time for all local devices.
- Observability: things should be able to fail silently and safely to backups. Of course, that's not as useful if I don't do something to rectify the failure, and if it's too silent I won't know to do something (or want to).

Oh, and of course, adding to this
- A blog.

Seeing as this is an introduction, I'm not really going to flesh those out right now, and I'll use other posts to explain them in greater detail. 

# Other Goals
Some people keep notes on their thoughts, and I've tried it too. Some of the best tools I've used are Obsidian and LogSeq, but I couldn't really ever get them to 'stick'--I have trouble getting myself in the habit of using them. Even if I do, I end up with page upon page of bulleted lists, and I think it might be helpful to put things in expository form. 

# AI and LLMs
For the most part, I don't intend to use LLMs. I have come to realize that some of my mannerisms come across as similar to what LLMs generate--such as em dashes--but if I use generative AI to make something, I will make it clear that I did so. Once I figure out tagging in this blog, I will tag posts that don't use AI for generating content as 'No AI'. I may still use AI as a copyeditor for such posts, but not to flesh out the content or to meet some word count. I may also use generative AI to create simplified summaries to explain more simply, but that would not be tagged as 'No AI'. 

There are probably more exceptions and nuance to it here, but I intend to flesh that out somewhere that is more of a living document than a static post. 