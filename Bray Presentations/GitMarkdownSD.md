---

marp: true
theme: gaia
math: katex
class: invert
paginate: true

style: |
    section.lead h1 {
        font-family: 'VictorMono Nerd Font Propo';
        font-size: 74px;
        font-style: bold;
        color: white;
        text-shadow: 2px 2px 0 #333;
    }

    section.lead h2 {
        font-family: 'VictorMono Nerd Font Propo';
        font-size: 48px;
        font-style: italic;
        color: white;
        text-shadow: 2px 2px 0 #333;
    }

    section.subsection {        
        text-align: center;
        justify-content: center;
        display: flex;
        flex-direction: column;
        height: 100%;
    }

    section.subsection h1{
        font-family: 'VictorMono Nerd Font Propo';
        font-size: 74px;
        font-style: bold;
        color: white;
    }

    section.subsection h2{
        font-family: 'VictorMono Nerd Font Propo';
        font-size: 48px;
        font-style: italic;
        color: white;
    }

---

<!-- _paginate: skip -->
<!-- _class: lead -->

![bg](thomas-griesbeck-BS-Uxe8wU5Y-unsplash.jpg)

# &#xe5fb; Version Control &#xF02A2;<br> Using Git

## How and When to Use Version Control

<footer>
    Last Edited: Jan 2024
</footer>

---

# Table of Contents

- [Basic Git Commands](#basic)

---

<!-- _class: subsection invert -->
<!-- _slide: #basic -->

![bg left:30% saturate:0.5](adam-vradenburg-sWAAhaoVuko-unsplash.jpg)

# Basic Git Commands

## &#xF401;init &#xEB3E;clone &#xEAFC;commit <br> &#xF403;push &#xEA64;pull  &#xEA77;sync

---

# git init

**Initializing a New Git Repository**

`git init` is a fundamental Git command used to start a new, empty Git repository or to reinitialize an existing one. When you run git init, Git creates a new subdirectory named `.git` in the root of your project directory. This `.git` directory contains all the metadata for the new repository — this metadata includes subdirectories for objects, refs, and template files, which are essential for the version control capabilities of Git.

---

# git init (cont'd)

Using git init is the first step in establishing a repository's version control environment. It does not create any project files themselves but sets up the necessary infrastructure so Git can start tracking changes to existing files or new files you add.

It’s important to note that git init is a safe command to run: it won't overwrite things that are already there. If you run git init in an existing directory, it will simply add the Git repository structure to this directory, enabling version control.

---

## Key Files to Commit

- **README.md**: Provides an overview of your project, how to set it up, and use it.
- **.gitignore**: Specifies intentionally untracked files to ignore (e.g., log files, build directories).
- **LICENSE.md**: States the license under which your project is made available (e.g., MIT, GPL).

---

## Using git init in Bash

To initialize a new Git repository in bash, navigate to your project directory and run:

```bash
cd /path/to/your/project
git init
```

This creates a new subdirectory named `.git` that contains all of your necessary repository files.

---

## Using git init in VS Code

1. Open your project folder in VS Code.
2. Open the integrated terminal (`Ctrl+``).
3. Run the `git init` command.

VS Code will recognize the repository and provide Git source control tools in the Source Control panel.

---

# git clone

---

# git commit

---

# git push

---

# git pull

---

# git sync

---

<!-- _class: subsection invert -->

# &#xEBD8; Azure DevOps &#xEBE8;

## Keeping Repositories Safe

---




---

<!-- _class: subsection invert -->

![bg left:30% saturate:0.6](geranimo-qzgN45hseN0-unsplash.jpg)

# Advanced Git Commands

---
