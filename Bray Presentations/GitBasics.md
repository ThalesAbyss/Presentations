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

    section.tight-slide p, 
    section.tight-slide li, 
    section.tight-slide h2 {
        font-size: 90%;
    }

    section.xtight-slide h1 {
        font-size: 95%;
    }

    section.xtight-slide p, 
    section.xtight-slide li, 
    section.xtight-slide h2 {
        font-size: 85%;
    }

    section.table-slide table{
        font-size: 60%;
    }

    footer {
        font-family: 'VictorMono Nerd Font Propo';
        font-weight: bold;
    }

---

<!-- _paginate: skip -->
<!-- _class: lead -->

![bg](thomas-griesbeck-BS-Uxe8wU5Y-unsplash.jpg)

# &#xe5fb; Code Historian &#xF02A2;<br> With Git

## Basic Commands for Version Control

<footer>Last Edited: Jan 2024</footer>

---

<!-- _class: subsection invert -->

![bg left:30% saturate:0.5](adam-vradenburg-sWAAhaoVuko-unsplash.jpg)

# Basic Git Commands

## &#xF401;init &#xEB3E;clone <br> &#xEADC;add &#xEAFC;commit &#xF403;push <br> &#xF418;branch &#xEAFE;merge

---

# `git init`

**Initializing a New Git Repository**

`git init` is a fundamental Git command used to start a new, empty Git repository or to reinitialize an existing one. When you run git init, Git creates a new subdirectory named `.git` in the root of your project directory. This `.git` directory contains all the metadata for the new repository — this metadata includes subdirectories for objects, refs, and template files, which are essential for the version control capabilities of Git.

<footer> &#xF401; init </footer>

---

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

This creates a new subdirectory named `.git` that contains all of your necessary repository files. GitHub (not git!) maintains a list of `.gitignore` templates: [GitHub .gitignore files](https://github.com/github/gitignore)

<footer> &#xF401; init </footer>

---

## Using `git init` in VS Code

1. Open your project folder in VS Code.
2. Open the integrated terminal (`Ctrl + (tilde)`)
3. Run the `git init` command.

-or-

1. Open your project folder in VS Code.
2. Click "Source Control" tab on the main toolbar
3. Click the button "Initialize Folder"

<footer> &#xF401; init </footer>

---

# `git clone`

This command initializes a new Git repository in the `local directory`, copies all the data from the `source repository` (including all versions of every file and branch), and sets up remote tracking branches for each branch in the cloned repository.

It also automatically creates a remote connection named `origin` pointing back to the original repository, making it easy to fetch updates or push changes back to it.

<footer> &#xEB3E; clone </footer>

---

You can clone repositories from various locations, including a local file system or remote servers like GitHub, GitLab, or Bitbucket. Additionally, `git clone` supports different transfer protocols like `HTTPS`, `SSH`, or Git's own protocol.

`git clone` is often the first step in contributing to a project, as it allows you to create a personal working copy where you can make changes _without affecting the original project_. Remember, any commits you make in your cloned repository are isolated to your local environment until you push them to a remote server.

<footer> &#xEB3E; clone </footer>

---

# `git add`

When you run:

```bash
git add <file1> <file2>
```

in your terminal, you're instructing Git to begin tracking changes made in your project. This command is the command for selectively preparing changes that are logged on your next `git commit` on your repository.

<footer> &#xEADC; add </footer>

---

- **Specific Files**: If you specify a file or files, Git stages only those files. This means only the changes in those files are marked for inclusion in your next commit.
- **All Current Changes**: Using `git add .` stages all the changes in your current directory and its subdirectories. This is a bulk operation that scoops up all modifications and new files (that are not in `.gitignore`) for staging.
- **Interactive Mode**: `git add -p` (patch mode) allows you to stage parts of files interactively, offering a granular level of control over your commits.

<footer> &#xEADC; add </footer>

---

In essence, `git add` doesn't automatically stage everything in your repository. It stages changes based on which command you use - be it specific files or all changes in your working directory.

Once staged, these changes are ready to be committed, creating a snapshot in your project's history.

<footer> &#xEADC; add </footer>

---

# `git commit`

Committing is a cornerstone of Git. Think of it as taking a snapshot of your project's current state, based on what's in the staging area. This snapshot includes all the changes you've staged with `git add`.

- **Commit Scope**: Only changes that are staged will be included in the commit. Unstaged changes remain in your working directory.
- **Immutable Snapshots**: Each commit is a permanent record in your project history. It has a unique ID (SHA-1 hash) that allows for tracking and reverting changes if needed.

<footer> &#xEAFC; commit </footer>

---

# Making a Commit

Creating a commit is more than just saving changes; it’s about documenting your project’s evolution. 

- **Basic Commit**: A simple `git commit` opens your default text editor for a commit message. 
- **Inline Message**: For quick commits, `git commit -m "Your message"` allows you to include a message directly in the command line.
- **Amendments**: Made a mistake in your last commit? `git commit --amend` lets you modify the most recent commit, whether to change the message or include additional changes.

<footer> &#xEAFC; commit </footer>

---

# Adding Commit Messages

Commit messages are vital for maintaining a readable history. They guide future contributors (including your future self) through the project’s development.

- **Clarity is Key**: Write clear, concise messages that describe the why and what of your changes.
- **Detailed When Needed**: For complex changes, include a brief summary in the first line, followed by a more detailed description after a blank line.

<footer> &#xEAFC; commit </footer>

---

# Commit Often

Committing often is a best practice in version control. Frequent commits:

- Help track and understand the history of changes more clearly.
- Make it easier to locate and fix bugs or revert to previous states.
- Facilitate collaboration by breaking down changes into manageable parts.

<footer> &#xEAFC; commit </footer>

---

# What `git commit` Doesn't Do

- `git commit` does not affect the remote repository. Changes must be pushed using `git push`.
- It doesn't automatically include all changes in your working directory; only staged changes are committed.
- `git commit` does not merge changes from different branches or resolve conflicts.

<footer> &#xEAFC; commit </footer>

---

<!-- _class: xtight-slide invert -->

# `git branch`

The `git branch` command is integral to managing the diverse development paths within a Git repository. Branches in Git are like parallel timelines for your project, allowing you to work on different features, fixes, or experiments separately from the main codebase.

- **Branch Creation**: Use `git branch <branch-name>` to create a new branch. This doesn't switch to the new branch, it only creates it.
- **Listing Branches**: Simply running `git branch` lists all the branches in your repository, with the current branch highlighted.
- **Branch Concept**: Branches are pointers to commits. Creating a new branch doesn't duplicate the code; it's a lightweight movable pointer to a specific commit.

<footer> &#xF418; branch </footer>

---

`git branch` is commonly used for safely implementing new features or fixing bugs, without disturbing the main codebase.

- **Feature Development**: Create a new branch for each new feature or significant change. This keeps your feature development isolated.
- **Bug Fixes**: Similar to features, create branches for working on bug fixes. This ensures that fixes can be tested without impacting the stable code.
- **Viewing Branches**: Use `git branch` to see all branches and `git branch -a` to view both local and remote-tracking branches.

<footer> &#xF418; branch </footer>

---

Effective use of branches is key to a well-managed and error-free workflow in Git.

- **Short-lived Branches**: Keep branches short-lived. Merge them back into the main branch once the feature or fix is complete and tested.
- **Naming Conventions**: Use descriptive names for branches (e.g., `feature/user-auth`, `fix/memory-leak`) for clarity.
- **Regular Merges**: Regularly merge changes from the main branch into your feature branches to minimize merge conflicts.
- **Prune Regularly**: Delete branches once they're merged into the main branch to keep the repository clean.

<footer> &#xF418; branch </footer>

---

<!-- _class: xtight-slide invert -->

# `git merge`

`git merge` is a command used to combine the changes from one Git branch into another. It's a fundamental tool for integrating different lines of development and is commonly used to bring together completed features or bug fixes into the main branch.

- **Merging Branches**: When you merge one branch into another, Git attempts to automatically combine the changes.
- **Fast-Forward Merge**: If there are no conflicting changes, Git performs a 'fast-forward' merge, simply moving the branch pointer forward.
- **Three-Way Merge**: If there are divergent changes, Git does a 'three-way merge', creating a new 'merge commit' that ties together the histories of both branches.

<footer> &#xEAFE; merge </footer>

---

<!-- _class: tight-slide invert -->

# Executing a Merge

Merging is a straightforward process but requires careful management to ensure smooth integration of code.

- **Initiating Merge**: To merge changes from one branch (e.g., `feature-branch`) into another (e.g., `master`), switch to the receiving branch (`git checkout master`) and then execute `git merge feature-branch`.
- **Handling Conflicts**: If there are merge conflicts, Git will pause the process, allowing you to resolve the conflicts manually. After resolving, you need to add and commit these changes.
- **Merge Completion**: Once all conflicts are resolved and committed, the merge is complete, and the branches are fully integrated.

<footer> &#xEAFE; merge </footer>

---

<!-- _class: tight-slide invert -->

# Merging Best Practices

Effective merging is crucial for maintaining a clean and stable codebase in Git.

- **Keep Branches Up-to-Date**: Regularly merge changes from the main branch into your feature branches to reduce conflicts.
- **Test Before Merging**: Always test the changes in your feature branch thoroughly before merging into the main branch.
- **Resolve Conflicts Carefully**: Take the time to carefully resolve merge conflicts. Incorrect conflict resolution can introduce bugs.
- **Clean Up**: After a successful merge, consider deleting the feature branch if it's no longer needed, to keep your repository tidy.

<footer> &#xEAFE; merge </footer>

---

<!-- _class: tight-slide invert -->

# `git push`

This command is used to upload your repository's changes to a remote repository. After committing your changes locally and merging branches, `git push` is how you share those changes, allowing your team to see and access the latest version of the code.

- **Uploading Commits**: `git push` uploads all local commits to the remote repository.
- **Synchronization**: This command helps keep your remote repository in sync with your local one.
- **Remote Repositories**: Typically, you'll push to a repository hosted on platforms like GitHub, Azure Repos, or Bitbucket.

<footer> &#xF403; push </footer>

---

<!-- _class: tight-slide invert -->

# Executing `git push`

Using `git push` is straightforward once you have committed your changes locally.

- **Basic Push**: Simply running `git push` will attempt to upload your commits to the remote repository connected to your current branch.
- **Specifying Remotes and Branches**: You can specify which remote and branch to push to with `git push <remote> <branch>`. For example, `git push origin master` pushes to the 'master' branch of the 'origin' remote repository.
- **Authentication**: You may be prompted for authentication (username and password or SSH key) to ensure secure transfer of code.

<footer> &#xF403; push </footer>

---

<!-- _class: subsection invert -->

![bg left:30% saturate:0.6](geranimo-qzgN45hseN0-unsplash.jpg)

# &#xEBD8; Azure DevOps &#xEBE8;

## Keeping Repositories Safe

---

... just kidding. We'll do this next time :smile:

<center>

![width:800px](https://media.giphy.com/media/3oEduNEbTtAHABX0dy/giphy.gif)

</center>

---

<!-- _class: table-slide invert -->

# Quick List

| Command    | Option     | Description                                                   |
|------------|------------|---------------------------------------------------------------|
| git init   |            | Initializes a new Git repository in the current directory.    |
| git clone  | `<url>`    | Clones a repository into a newly created directory.           |
| git add    | `<file>`   | Adds file contents to the staging area.                       |
|            | `.`        | Adds all files in current folder to staging area.
| git commit | `-m "<message>"` | Records file snapshots permanently in the version history. |
| git push   | `<remote> <branch>` | Uploads local repository content to a remote repository.  |
| git branch | `<branch>` | Creates a new branch.                                         |
| git merge  | `<branch>` | Merges a specified branch into the current branch.            |
