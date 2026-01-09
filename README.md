# Art Vault 

## Purpose

The purpose of this repo is to generate SSOT vaults for projects.

In this vault, the following elements will be present:
- Source Files
- Exported assets (to the desired project size)
- Relational table of assets (to check on a quick glance)
- Information on project asset management: compression rules, naming conventions, TextureImporter presets justification...

Having all in a single project will prevent:
- Dealing with multiple platforms (GDrive, Slack sharing, Confluence...)
- Having everything at reach
- Being aware at all times of the existing assets inside the game
- Being aware of how assets should be treated

A template folder structure is going to be provided as an example at master.

## Requirements

- [Github Account](https://github.com/login)
- [Obsidian](https://obsidian.md/download)
- [Git](https://git-scm.com/install/windows)
- _**(Optional)**_ Git UI of choice. We recommend [Sublime Merge](https://www.sublimemerge.com/)
## Methodology
### Project Management

This repo is going to be organised in a specific way:

- MASTER branch is protected and will only have the README file and other instruction files. This branch is protected and won't have any project-related content
- Each project is going to have its own BRANCH, having the project name as branch name. If any more branching is required, then the `<project-name/<branch-name>` convention will be followed

This structure is meant to prevent having unwanted assets or references to other projects; this way, every branch is gonna be a SSOT for a certain project, keeping everything encapsulated.

### Vault Management

A initial `.obsidian` folder with a set base of plugins is provided. The `.obsidian` file is ignored, but is already tracked, so won't ignore changes from the get-go. If any changes to the vault are needed, open a terminal at the folder and run this command first:

```bash
git ls-files -z .obsidian | xargs -0 -n 1 git update-index --skip-worktree
```

> [!info]- Command Explanation:
> ### 1️⃣ `git`
> 
> - This is the **Git command-line program** itself.  
> - All the subcommands (`ls-files`, `update-index`, etc.) are run through it.
> - Think of it as: “Hey Git, I want you to do something.”
> 
> ---
> 
> ### 2️⃣ `ls-files`
> 
> - A **Git subcommand**.  
> - It lists all files **currently tracked by Git** in the repository.
> - It does **not** list untracked files (these are ignored unless added).
> - So this is how we find all the `.obsidian` files Git is aware of.
> 
> ---
> 
> ### 3️⃣ `-z`
> 
> - Option to `git ls-files`.
> - Outputs filenames **separated by a null character (`\0`)** instead of newlines.
> - Why? Safe for filenames that contain **spaces, quotes, or special characters**.
> - This prevents errors when feeding filenames into other commands (like `xargs`).
> 
> ---
> 
> ### 4️⃣ `.obsidian`
> 
> - This is a **path argument** passed to `git ls-files`.
>     
> - It tells Git: “Only list tracked files **inside the `.obsidian` directory**.”
>     
> - Git will recurse automatically, so it lists **all files inside `.obsidian/` and its subdirectories**.
> 
> ---
> 
> ### 5️⃣ `|` (pipe)
> 
> - This is a **shell feature**, not Git.
>     
> - It takes the **output of the command on the left** and feeds it as **input to the command on the right**.
>     
> - Here: the list of `.obsidian` files from `git ls-files` is sent to `xargs`.
> 
> ---
> 
> ### 6️⃣ `xargs`
> 
> - A **Unix command-line tool** that takes input (usually a list of items) and runs a command with those items as arguments.
> - Useful for converting a list of lines into **command-line arguments**.
> - Here, it’s used to call `git update-index` on **each file from the list**.
> 
> ---
> 
> ### 7️⃣ `-0`
> 
> - Option to `xargs`.
> - Tells `xargs` to **expect null-terminated input** (`\0`) instead of newline-terminated input.
> - Works together with `-z` from `git ls-files`.
> - Ensures filenames with spaces, quotes, or special characters are handled correctly.
> 
> --- 
> 
> ### 8️⃣ `-n 1`
> 
> - An option to `xargs`.
> - Means: **run the command once for each input line**.
> - Without `-n 1`, `xargs` might try to pass **all files at once**, which can fail if:
  >   - There are too many files
  >   - Filenames have spaces or special characters
> - `-n 1` ensures each file is processed **individually**, which is safer.
>
> ---
> 
> ### 9️⃣ `git update-index`
> 
> - Another Git subcommand.
> - Used to **manipulate Git’s index (the staging area)**.
> - Normally, you use it to add, remove, or change how Git tracks a file without touching the working directory.
>
> ---
>
> ### 🔟 `--skip-worktree`
> - An option to `git update-index`.
> - Tells Git: “I want this file to **stay tracked in the repo**, but **ignore any local modifications**.”
> - Local changes to these files will no longer show up in `git status` or be staged by default.
> - Important: this **does not prevent someone from forcing a commit** with `git add -f`, but it covers your usual workflow.

 With this command, each and every user is free to configure their obsidian vault as they please without changes being reflected on the git history.

## Further Improvements

### Asset Management
[Adonis Sigua](https://github.com/adsiguatripledot) sugested that, since this is going to act as a SSOT for art in projects, that we can generate some kind of asset management tool parting from here; maybe generating a github action that on push updates some assets in a bucket or in a package that the project reads so assets are auto-updated.

This can collide with quickly adding assets to the project locally, so will potentially generate a drawback in speed for prototypes, but it's a nice way to keep projects tidy, clean and with asset awareness.
