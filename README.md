# [Sparrow landing page repo](https://trysparrow.com)
## Git usage
If you're using Atom, you can use their GUI (graphical user interface) for git. This tutorial will use the git CLI (command line interface).
### First time
Get repository locally by running
`git clone https://github.com/trysparrow/sparrow-landing.git`

<set user information>
### Each time you work something new
Switch to master branch
`git checkout master`

Get the latest version
`git pull`

Make your own branch for your changes
`git checkout -b <branch-name>`
Branch names should be all lower case with words separated by hyphens and should very briefly surmize what your changes will be. Also see project conventions section before naming branches.

Now you're prepared to make your changes! See the next section for recording your changes in git, and return here once you're ready to have your changes brought into the master branch.

===

Go to the repository on the Github website (where you're probably reading this), and click on the `Pull requests` tab.

Click the yellow/green button to make a pull request.

Write a clear title and description and submit.

On the right side, add Deborah as a reviewer.

If your pull request resolves an issue, comment `resolves #<issue number>`.

Wait for Deborah to approve the pull request or to request changes.

AFTER the pull request is approved, press the button to merge your changes, and press the button to delete your branch.

Congratulations!! Your contribution is now part of the main codebase in the master branch.
 
### Each time you make a change of substance
See the state of git
`git status`

Stage your changed files
`git add <path/to/file> [path/to/another/file]`

Record your changes in git
`git commit -m"<write sentence describing your changes in present tense>"`

IF `git status` only shows changed files you want to record, you can skip adding files and use the `-a` flag before `-m` to automatically stage all changed files before commiting.

Share your changes to Github
`git push`
If you are prompted to create the remote branch, copy and paste the provided command and run it.


### Project conventions
Prefix branches for new features and new site pages with `f-`  
Prefix branches for updating content like new blog posts, typo fixes, and changing images with `u-`  

## Jekyll usage
### Writing new blog posts
#### Filename
Blog posts are saved under `/_posts/` and are named by publish date and post name. Names should be all lower-case.
`/_posts/yyyy-mm-dd-post-name.md`
#### Front matter
New blog posts should copy and fill in the front matter from old ones. Preview is optional and will default to banner.
`<>` indicates a required field.
`[]` indicates an optional field.
```
---
layout: post
title: "<blog post title>"
authors:
 - <author ID (e.g. debh)>
 - [additional authors]
mins_read: "<rough number of minutes to read post>"
description: "<short description to show in previews. avoid anything that runs out of box in blog post listing>"
preview: "[filename in path /assets/images/banners. will default to banner]"
banner: "<filename in path /assets/images/banners>"
permalink: "/blog/<post permenant url ending>"
---

```
The blank line between front matter and content is required.
#### Content
Jekyll posts can be written in a mix of Markdown and HTML.

### Faces and authors
Authors and everyone with a name and photo are listed in _data\/people.yml by the first three letters of their given name and first letter of their surname. For instance, our benevolent overlord would be debh. I don't know why I made this so complicated.

### Image assets layout
\/assets\/images
 - \/banners: Banners and post preview pictures
 - \/faces: Headshots of folks in people.yml
 - \/figures: Diagrams and stuff to illustrate stuff
 - \/world: People doing stuff in the world (I'm bad at directory names)

