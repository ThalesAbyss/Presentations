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

    footer {
        font-family: 'VictorMono Nerd Font Propo';
        font-weight: bold;
    }

---

<!-- _paginate: skip -->
<!-- _class: lead -->

![bg](thomas-griesbeck-BS-Uxe8wU5Y-unsplash.jpg)

# &#xe5fb; Version Control &#xF02A2;<br> Using Git

## How and When to Use Version Control

<footer>Last Edited: Jan 2024</footer>

---

<!-- _class: subsection invert -->

![bg left:30% saturate:0.5](adam-vradenburg-sWAAhaoVuko-unsplash.jpg)

# Basic Git Commands

## &#xF401;init &#xEB3E;clone &#xEAFC;commit <br> &#xF403;push &#xEA64;pull  &#xEA77;sync

---

# `git init`

**Initializing a New Git Repository**

`git init` is a fundamental Git command used to start a new, empty Git repository or to reinitialize an existing one. When you run git init, Git creates a new subdirectory named `.git` in the root of your project directory. This `.git` directory contains all the metadata for the new repository — this metadata includes subdirectories for objects, refs, and template files, which are essential for the version control capabilities of Git.

<footer> &#xF401; init </footer>

---

# `git init` (cont'd)

Using `git init` is the first step in establishing a repository's version control environment. It does not create any project files themselves but sets up the necessary infrastructure so Git can start tracking changes to existing files or new files you add.

It’s important to note that `git init` is a safe command to run: it won't overwrite things that are already there. If you run `git init` in an existing directory, it will simply add the Git repository structure to this directory, enabling version control.

<footer> &#xF401; init </footer>

---

## Key Files to a Repository

- **`README.md`**: Provides an overview of your project, how to set it up, and use it.
- **`.gitignore`**: Specifies intentionally untracked files to ignore (e.g., log files, build directories).
- **`.gitattributes`**: Used to define the attributes to be used by Git for certain file paths in the repository. It can control things like line ending normalization, diff settings, and merge strategies for specific files and directories.
- **`LICENSE.md`**: States the license under which your project is made available (e.g., MIT, GPL).

<footer> &#xF401; init </footer>

---

## Using `git init` in a Terminal

To initialize a new Git repository in bash, navigate to your project directory and run:

```bash
cd /path/to/your/project
git init
```

This creates a new subdirectory named `.git` that contains all of your necessary repository files.

<footer> &#xF401; init </footer>

---

## Using `git init` in VS Code

1. Open your project folder in VS Code.
2. Open the integrated terminal (`Ctrl + (tilde)`)
3. Run the `git init` command.


VS Code will recognize the repository and provide Git source control tools in the Source Control panel.

<footer> &#xF401; init </footer>

---

# `git clone`

This command initializes a new Git repository in the `local directory`, copies all the data from the `source repository` (including all versions of every file and branch), and sets up remote tracking branches for each branch in the cloned repository.

It also automatically creates a remote connection named `origin` pointing back to the original repository, making it easy to fetch updates or push changes back to it.

---

# `git clone` (cont'd)

One of the important aspects of `git clone` is its flexibility. You can clone repositories from various locations, including a local file system or remote servers like GitHub, GitLab, or Bitbucket. Additionally, `git clone` supports different transfer protocols like `HTTPS`, `SSH`, or Git's own protocol.

`git clone` is often the first step in contributing to a project, as it allows you to create a personal working copy where you can make changes _without affecting the original project_. Remember, any commits you make in your cloned repository are isolated to your local environment until you push them to a remote server.



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

![bg left:30% saturate:0.6](geranimo-qzgN45hseN0-unsplash.jpg)

# &#xEBD8; Azure DevOps &#xEBE8;

## Keeping Repositories Safe

---
