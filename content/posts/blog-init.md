+++
title = 'Blog.init'
date = 2025-10-14T12:49:32-04:00
+++

I never gave much thought to making a blog, but more recently, I've been coming across things for which there is little or no good documentation. So, I thought why not?

# Background
Of course, then I started to think more about it and realized that it would be a good way for me to keep track of projects. Nothing I do has been quick, and there's always more I *could* do, so I thought that writing down whatever I was working on and documenting my thoughts might help me put down and later pick a project back up. Lately, I've been working on a Rust-based implementation of PTP, but it's taken me longer than I expected... or rather the scope has creeped.{{% sidenote %}} Because of *course* it has {{% /sidenote %}}

I've also looked at other platforms for blogging, and I found [Hugo] which is mostly what I'd expect a blogging platform to be, if not more involved than what I had initially hoped. However, it also gives me a great deal of control (perhaps to my own detriment) and now publishing this blog has become an endeavor and project in its own right.

Of course, if this is meant to be my own notes as well, then I want the pages to represent the way that I think about things. To that end, I find that I like toneboxes, marginalia, and other distractions. Hugo provides me the capability to customize just about everything, and none of it seems ot be a requirement that it's a good idea, just like ca. 2004 MySpace. But, more importantly, it requires no database and mostly uses plain-text files that are readable in their own right to generate the 'content'. I think that databases are all too often overused, and a blog is no exception.

## Ethos
Not sure if 'ethos' is the right word, but there are a few things that I want to set out as more or less immutable expectations. 

Without discussing my personal philosophy on the AI-du-jour, I should make it clear that I see AI as a tool, and often over-used. I can and will use AI, but not to turn a summary or list or idea into a blog post. Nothing here will be outright AI-generated, but there will be much that is refined by AI. I'm also terrible at graphics, so I'd expect that you'll see AI-generated images, charts, and diagrams. I'm still figuring it out, but I intend to label such diagrams, even if I end up editing or refining them.

There's no guarantee that starting a project will see it through to the finish line, but at least knowing my last position on the project should help.

Finally, the Oxford comma is not a suggestion.

## Style
One appealing thing about Hugo is the ability to arbitrarily style... anything.{{% sidenote %}} This also seems to be to it's own detriment, but nevertheless seems a slight net-positive. {{% /sidenote %}} Hugo is mostly a templating engine, and so it renders markdown (or other) files into HTML, which are nice static pages. Those are from templates. This means that I can (try to) modify them to fit my style. Already, I've had to modify the Blowfish theme to support custom SCSS (so that I can customize the colors more easily), and I'll probably write about that later. But, I want the articles that I post here to not just represent my thoughts in an expository format, but I'd like it to somewhat mimic the way that I think. So, the theme and features should evolve as I figure out Hugo, Blowfish, CSS, and other things. I want you to understand not just *what* I'm thinking, but *why* and *how* I thought it.

### Sidenotes
One thing that I made work first was sidenotes. They're used in this article, and I'll probably include more in a later post, but know that it's mostly CSS, although inspired heavily by a few resources[^1] [^2] [^3]

[Hugo]: https://www.gohugo.io
[^1]: https://danilafe.com/blog/sidenotes/
[^2]: https://scripter.co/sidenotes-using-only-css/
[^3]: https://scottstuff.net/posts/2024/12/16/sidenotes-in-hugo-with-fixit/