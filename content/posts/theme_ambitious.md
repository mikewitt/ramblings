---
date: '2025-11-09T23:37:06-05:00'
draft: true
title: 'Theme: Ambitious'
tags:
  - hugo
  - ambitious theme
params:
  epigraph:
    source: The Programmer's Credo, Author Unknown, Parody of John F. Kennedy
    text: We do these things not because they are easy, but because we thought they would be easy.
  acronyms:
    css:
      definition: "Cascading Style Sheets"
      term: CSS
---

I've built a new theme, which I'm calling 'ambitious' because I was being overly ambitious when I did so.

## Why?

Not much to it other than that. I realized I wanted control over the styling of my pages, and forking or modifying an existing theme wouldn't be sufficient. So, after much deliberation, I decided it would be easier to learn CSS and JavaScript, and write my own template. I did borrow heavily from [blowfish](https://blowfish.page), as there were quite a few elements there that I liked. However, there were plenty that I didn't like or couldn't easily override. Additionally, Tailwind has a new version and updating to it is not trivial. Similarly, Blowfish itself is stuck using a legacy layout for their template. Hugo does continue to support the old structure but the new structure introduced is vastly different. Not that the Hugo documentation is good (it isn't bad, but it's somehow both sparse and complete at the same time), but that it doesn't line up with the Hugo documentation made it similarly painful to work with.

## What's next?

I'm going to continue to tweak and update the theme with my own preferences now, but it only took a few weeks worth of work to get it to a working state at least. Updates should continue as long as I need it. The theme is publically available, and if anyone has any issues with it and wants to use it, feel free to reach out through Github.

## What's wrong?

This has revealed some shortcomings of Hugo (for me, at least). 

There is no native way to modify many of the things that you might want to. For example, we can create the Table of Contents (seen at left), using the template command `{{ .TableOfContents }}` which renders headings to be a list of items. However, it also still renders **even if** we have no items. So, if we want to selectively render the Table of Contents, if there are headings, we need to do some fancy-schmancy things to figure out *if we have headings in the first place*. But, more than that, if we want to modify the children to have class definitions... we can't.

And, we're given some methods, especially `PAGE.Fragments.HeadingsMap` which can give us a mapping of headings, IDs, and more; everything we might need to render the Table of Contents... but then we have no way to access the usual configuration for it. Normally it would be in the [config>markup.tableOfContents](https://gohugo.io/configuration/markup/#table-of-contents). But, although we're given the method [`PAGE.Site.Config`](https://gohugo.io/methods/site/config/), it doesn't give us access to the tableOfContents parameters. So, we need to store them somewhere we can access them.

Regex in Go (and therefore, Hugo) sucks. There are no backreferences, lookaheads, or lookbehinds. So, replacing text in something is rather limited--still mostly functional--but there are a number of cases where it would be extremely helpful to be able to leverage such tools to make the regex more simple.{{% sidenote %}} For some definitions of 'simple' {{% /sidenote %}}

Of course, I understand some/all of these shortcomings are in the name of 'security', and I can kind of appreciate that. But, at the same time, it would take a really weird use case to be able to alter that, no? And it still doesn't let you modify files on the system, so you can't modify the repo containing your documents using this.