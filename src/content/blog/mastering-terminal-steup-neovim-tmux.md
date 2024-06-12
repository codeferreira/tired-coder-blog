---
author: Jose Ferreira
pubDatetime: 2024-06-12T16:22:00Z
modDatetime: 2024-06-12T16:22:00Z
title: "Mastering the Terminal: My Developer Setup with Neovim and Tmux (Part 1)"
slug: mastering-terminal-setup-neovim-tmux
featured: false
draft: true
tags:
  - setup
  - neovim
  - tmux
  - terminal
description: Explore my journey in transitioning to a terminal-centric development environment with Neovim and Tmux. Learn about the tools, configurations, and insights that have optimized my workflow.
---

### Introduction

As a Software Engineer with over eight years of experience, I've had the opportunity to work on various applications impacting thousands of users. Throughout my career, I've mostly worked with JavaScript but have also dabbled in Python, Golang, and other technologies.

I wanted to share my experiences through this blog. My goal is to create a journal of my professional life, my explorations, my setup, and the things I enjoy. This blog is not about teaching but rather about documenting my journey, inspired by the content of Fabio Akita and the idea of the Henry Jones Diary from Indiana Jones. It's a way to look back years later and understand my knowledge base at different points in time.

### Core Tools and Their Evolution

#### Previous Setup

Before fully transitioning to a terminal-based workflow, I experimented with several popular code editors. My journey began with Sublime Text, renowned for its speed and simplicity. I then moved to Brackets, a now lesser-known gem by Adobe that offered a unique live preview feature, revolutionary at the time. Atom was next, providing a highly customizable experience with its vast library of plugins. Eventually, I adopted VSCode, which quickly became my go-to editor due to its robust features and active community support.

During this period, my focus was not particularly on optimizing my workflow or increasing typing speed. I enjoyed customizing my environment to be visually appealing and exploring new tools. However, constantly chasing the "next big thing" wasn't necessarily making me a better developer. This realization set the stage for a more thoughtful approach to my development setup.

![Previous Setup](/images/keyboard_86.png)
Description: Screenshot of previous setups using Sublime Text, Atom, and VSCode.\_

#### Neovim

My journey with Neovim began in earnest in 2022 when I decided to repurpose an old Mac mini as a Linux desktop. While VSCode was functional, it was too resource-intensive for my needs. I needed a lightweight setup that could run efficiently on my Mac mini with a minimal Linux distribution. This led me to explore Neovim, specifically LunarVim, which promised an IDE-like experience without the heavy resource usage.

Initially, I had many misconceptions about Vim. I thought it was too difficult and only suitable for pro developers with decades of experience. I believed it would slow me down initially to eventually speed me up, but the reality was more balanced. It was challenging but manageable. I kept a cheatsheet of basic Vim commands open in my browser and referred to it frequently. As I used it daily, it gradually became more intuitive.

![Cheatsheet](/images/keyboard_86.png)
Description: Screenshot of a Vim cheatsheet used during the initial learning phase.\_

The turning point was watching YouTube videos showcasing various setups and realizing the power and extensibility of Vim. The need for a lightweight editor on my improvised Linux setup also played a crucial role. What truly made me stick with Vim was the powerful movement commands and the vast extension capabilities.

![YouTube Setup Video](/images/keyboard_86.png)
Description: Screenshot or link to a YouTube video that inspired the transition to Neovim.\_

#### Testing Neovim Distributions

I experimented with several Neovim distributions, each offering unique features. While most distributions are similar in functionality, they differ in how they handle plugins and configurations:

- **LunarVim**: My first attempt at using Neovim. It was feature-rich but difficult to customize and upgrade, leading to some frustration.
- **LazyVim**: A more lightweight and simpler distribution. I appreciated its minimalism and ease of use.
- **NvChad**: Another distribution I tested, which offered a good balance of features but didn't fully meet my needs.

Ultimately, I settled on AstroNvim due to its vibrant community and extensive packs and pre-configured setups that made it easy to start with Neovim. The combination of an IDE-like experience in a simple config I could clone from GitHub was compelling. Additionally, having my configurations stored and shared across devices with ease of tracking changes was a significant advantage over my previous experiences with VSCode's sync.

![AstroNvim Screenshot](/images/keyboard_86.png)
Description: Screenshot of AstroNvim with customized configurations.\_

#### Learning Vim Motions and Macros

Learning Vim motions was not easy, but it has become second nature. I often find myself trying to use Vim motions in other applications, like Slack or WhatsApp, instinctively. My approach was gradual, starting with a Vim plugin for VSCode to learn without abandoning my setup. This allowed me to get comfortable with Vim motions while working, easing the transition.

I used the Learn Vim plugin on VSCode for a while, which was a good starting point. However, I prefer learning by doing. I attempted tasks, failed, and then searched for solutions, which helped me learn from my mistakes and solidify my understanding.

Macros are another powerful feature I've started to explore. While I'm still at the beginning of this journey, I've learned to create simple macros to automate repetitive tasks, such as adding quotation marks around text or changing the case of letters across multiple lines. Recording a macro and playing it back with a single key press has been a significant productivity boost.

![Vim Motions](/images/keyboard_86.png)
Description: Screenshot or diagram illustrating basic Vim motions.\_

#### Favorite Features and Plugins

Some of my favorite plugins include:

- **Telescope Fuzzy Finder**: Helps me find files or folders quickly.
- **Spectre nvim**: For search and replace operations.
- **Refactoring from Primeagen**: Simplifies code refactoring and moving code around.
- **Supermaven**: A good alternative to GitHub Copilot, though I still need to configure it properly with Nvim CMP.
- **Toggle Term**: Allows me to open a terminal inside Neovim for quick commands or running CLI tools like lazygit.

Most of my plugins are related to the languages I use, such as linters, formatters, and debuggers. While I don't miss any major IDE features, I'm still working on perfecting multi-cursor support in Neovim.

![Telescope Fuzzy Finder](/images/keyboard_86.png)
Description: Screenshot of Telescope Fuzzy Finder in action.\_

### Tmux

#### Initial Interest and Adoption

The motivation to start using Tmux was to leverage hardware-accelerated terminal emulators like Alacritty while managing multiple shells within a single application instance. Although terminal emulators like WezTerm and iTerm2 offer similar features, Tmux's customizability and plugin support for session persistence set it apart.

My first impressions were that I was not utilizing Tmux's full potential. Initially, I used it to create tabs, windows, and sessions to organize my workflow, such as having a window for the frontend with panes for Neovim and running commands. However, I realized there was more I could do to enhance my workflow further.

![Tmux Setup](/images/keyboard_86.png)
Description: Screenshot of a basic Tmux setup with multiple windows and panes.\_

#### Session Creation and Management

In my daily work, I manage three main repositories: frontend, backend, and data. I set up a Tmux session for each repository, typically with windows for Neovim and running the server. Each window is divided into panes, with the larger pane for Neovim and smaller panes for running tests or commands. This organization allows me to switch contexts quickly and maintain a structured workflow.

![Tmux Session](/images/keyboard_86.png)
Description: Screenshot of a Tmux session with multiple windows and panes for frontend, backend, and data repositories.\_

#### Integrated Terminal in Neovim

I leverage the integrated terminal in AstroNvim, using Toggle Term, for quick commands like installing dependencies or executing CLI tools. This setup reduces context switching and keeps my workflow efficient.

![Integrated Terminal](/images/keyboard_86.png)
Description: Screenshot of an integrated terminal within Neovim using Toggle Term.\_

#### Tmux Configuration

My Tmux configuration is straightforward, incorporating Vim motions in visual mode and using a basic Catppuccin theme for aesthetics. I've also remapped some keybindings to suit my keyboard layout better, changing the default leader key to `CTRL+A` for easier access on my Sofle v2 keyboard.

![Tmux Configuration](/images/keyboard_86.png)
Description: Screenshot or text snippet of key parts of the Tmux configuration.\_

For those interested in more details, I have a repository with my Tmux configuration which can be found [here](https://github.com/your-tmux-config).

#### Plugins and Session Persistence

The setup for `resurrect` and `continuum` plugins is based on their standard documentation. This setup allows me to save sessions and restore them automatically, providing continuity even after a system reboot. This feature has been a lifesaver during power outages or system restarts, saving time and maintaining my workflow without disruption.

![Tmux Plugins](/images/keyboard_86.png)
Description: Screenshot of Tmux session persistence in action.\_

### Personal Touch and Advice

The biggest highlight of my transition to a terminal-centric setup is the speed and efficiency I've gained. Moving around without a mouse, finding files quickly, and accessing code with simple shortcuts have all contributed to a more streamlined workflow. While the primary motivation was personal satisfaction and the challenge of learning something new, the practical benefits have been significant.

For those considering a similar transition, here are some tips:

- **Start with a Neovim Distribution**: Pick a distribution like AstroNvim, NvChad, LazyVim, or LunarVim. Test it out, embrace the frustration of learning, and enjoy the discovery process.
- **Use Vim Motions in Your Current Editor**: Most popular editors have a Vim plugin. Use it to get accustomed to Vim motions while working in a familiar environment.
- **Gradual Transition**: Don't rush to master everything at once. Focus on the basics first, then gradually explore advanced features.

![Learning Vim](/images/keyboard_86.png)
Description: Screenshot of using Vim motions in a popular code editor.\_

### Conclusion and What's Next

Transitioning to a terminal-centric setup with Neovim and Tmux has been a transformative experience for my development workflow. The journey has been filled with learning, customization, and a newfound appreciation for efficient, lightweight tools. This first part of my series has covered the core tools that form the backbone of my setup.

In the next part of this series, I'll dive into the additional tools and utilities that complement Neovim and Tmux, making my workflow even more powerful and efficient. We'll explore terminal emulators, shell and prompt configurations, and a suite of CLI tools that enhance my daily productivity.

Stay tuned for more insights and detailed configurations in the upcoming posts!
