---
layout: page
title: "How I Build This"
date: 2015-09-28 09:42 PM
comments: true
sharing: true
footer: true
---

Octopress offers some rake tasks to create post and pages preloaded with metadata and according to Jekyll's naming conventions. It also generates a global and a category based feed for your posts (You can find them in `atom.xml` and `blog/categories/<category>/atom.xml`).

If you are using zsh in the command line, then please add `alias rake=noglob` rake to your zsh config to prevent the `zsh: no matches` found error that occurs when running these rake tasks.

## Blog Posts

Blog posts must be stored in the `source/_posts` directory and named according to Jekyll's naming conventions: `YYYY-MM-DD-post-title.markdown`. The name of the file will be used as the url slug, and the date helps with file distinction and determines the sorting order for post loops.

Octopress provides a rake task to create new blog posts with the right naming conventions, with sensible yaml metadata.

### Syntax

```
rake new_post["title"]
```
The `new_post` command expects a naturally written title and strips out undesirable url characters when creating the filename. The default file extension for new posts is `markdown` but you can configure that in the `Rakefile`.

Note: some command line interpreters, e.g. zsh, have a special meaning for `[` and `]` so you have to escape them or temporary switch to bash.

### Example

```
rake new_post["Zombie Ninjas Attack: A survivor's retrospective"]
# Creates source/_posts/2011-07-03-zombie-ninjas-attack-a-survivors-retrospective.markdown
```
The filename will determine your url. With the default permalink settings the url would be something like `http://site.com/blog/2011/07/03/zombie-ninjas-attack-a-survivors-retrospective/index.html`.

Open a post in a text editor and you'll see a block of yaml front matter which tells Jekyll how to processes posts and pages.

``` yaml
---
layout: post
title: "Zombie Ninjas Attack: A survivor's retrospective"
date: 2011-07-03 5:59
comments: true
external-url:
categories:
---
```
