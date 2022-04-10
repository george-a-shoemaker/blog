---
layout: single
title:  "How the hell to exit Vim"
date:   2022-04-09 12:00:00 -0600
categories: software
---

\~ or \~ a design critique of the text editor we love to hate, Vim.
<p align="center">
   <img
      src="{{ site.url }}{{ site.baseurl }}/assets/images/vim-logo.png" alt="Logo of Vim text editor"
   >
</p>

## A common scenario

🐥 You're a spring chicken dabbling in `git` and you want to make your first commit.  
 `git commit -a`

Odds are `git` just fired up Vim and you're expected to:

1. Write your commit message
2. Save you commit message
3. Exit Vim

When you start typing your message, things get wackadoodle. The mouse is useless. You panic. 😱

Google tells you to:

1. Write your commit message
   - Type `i` to enter "insert mode"
   - Type out your commit message
2. Save your commit message
   - Hit `esc` to return to "normal mode"
   - Type `:w` and hit `enter` to "write" the file
3. Exit Vim
   - Type `:q` and hit `enter` to quit Vim

What the hell was all that?

If you never want to experience that again you can configure `git` to use easy peasy `gedit`:  
`git config --global core.editor "gedit -w -s"` 

## A design critique of Vim

I've been reading [The Design of Everyday Things][design-of-wiki] by Don Norman. I'll be using some terminology from the first chapter to describe what's good and bad about Vim.

## Yes, I actually use Vim

Here's why.

It's nearly ubiquitious on Unix-like systems. It'll make you dangerous on a remote server with no GUI. If Vim isn't installed look for it's predecessor, Vi.

I also use Vim keybindings across IDEs, namely Xcode / Android Studio / VS Code. I know these editors have good shortcuts, I just don't want to learn a new set for each one.

Vim is simply what I'm used to. A professor in college introduced me to it and I dove in.

## Should you learn Vim?

I'll leave that up to you. It takes real effort to make it useful.

I suggest learning with [vim.so][vim-so]. It's interactive and helps you internalize the keystrokes with repetition.

[vim-so]:https://www.vim.so/
[design-of-wiki]:https://en.wikipedia.org/wiki/The_Design_of_Everyday_Things