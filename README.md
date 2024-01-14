# git-master-class-task

## Explain version control.

**Version control is a system that tracks and manages changes to files over time, like an undo button and history log for your code, documents, or other files.** It's primarily used in software development, but also benefits other fields.

**Key benefits:**

- **Preserves history:** You can revert to previous versions, review changes, and track progress.
- **Enables collaboration:** Multiple people can work on the same files, merge changes, and resolve conflicts.
- **Enhances experimentation:** Try new things without fear of losing work, as you can easily revert if needed.
- **Provides backup and disaster recovery.**
- **Helps track and organize changes.**

**How it works (simplified):**

1. **Create a repository** to store your project's files and history.
2. **Commit changes** to save snapshots of the current state with descriptive messages.
3. **Create branches** for different features or bug fixes, and merge them back later.
4. **Review history** to see past changes, compare versions, and identify who made edits.
5. **Revert to earlier versions** if needed.

**Common version control systems:** Git, Subversion (SVN), Mercurial.

## Explain difference between git and github

**Git:**

- **Software:** A **distributed version control system (DVCS)** that runs on your local machine.
- **Functionality:** Tracks changes in files, lets you create snapshots (commits) with messages, and revert to previous versions.
- **Purpose:** Manage local versions of your code and collaborate with others by sharing repositories.
- **Ownership:** Open-source, free to use and modify.
- **Example:** Think of it like a detailed journal for your code changes, stored on your laptop.

**GitHub:**

- **Service:** A **web-based platform for hosting Git repositories**.
- **Functionality:** Provides online storage for your Git repositories, allows collaboration through features like pull requests and issue tracking.
- **Purpose:** Share your code publicly or privately, collaborate with others, and showcase your projects.
- **Ownership:** Owned by Microsoft, offers both free and paid plans.
- **Example:** Think of it as a cloud storage for your Git journal, allowing others to access and contribute.

**In simpler terms:**

- **Git is the tool you use to track changes (like a journal on your own computer).**
- **GitHub is the place where you store and share your Git journal (like a public notebook or cloud storage).**

## List 3 other github alternatives

Here are 3 popular alternatives to GitHub, each with its own strengths:

1. **GitLab:**

   - **Key features:** All-in-one platform for planning, building, and shipping software, including code hosting, issue tracking, CI/CD pipeline, and project management tools.
   - **Strengths:** Robust feature set, ideal for managing DevOps workflows, good free plan with private repositories.

2. **Bitbucket:**

   - **Key features:** Code hosting platform with strong focus on code review and collaboration, tight integration with other Atlassian tools like Jira and Confluence.
   - **Strengths:** User-friendly interface, excellent code review tools, seamless integration with Atlassian ecosystem.

3. **Gitea:**
   - **Key features:** Self-hosted Git hosting platform, forked from Gogs and offering a lightweight, easy-to-deploy solution.
   - **Strengths:** Open-source and free, customizable, suitable for developers who prefer self-hosting their code.

## Explain the difference between git fetch and git pull,

- **`git fetch`** is like downloading new files from the central storage to your workspace. It downloads all the latest changes from the remote repository **but doesn't apply them to your active files.** These downloaded changes sit in a separate area, waiting for your instructions. It's like getting the latest books delivered to your desk but not putting them on the shelves yet.

- **`git pull`** is like fetching those new files _and_ putting them on the shelves in your workspace. It combines the actions of `fetch` and a `git merge` command. It downloads the latest changes from the remote repository and **immediately merges them into your current branch.** This updates your active files, integrating the new changes into your ongoing work. It's like getting the new books, sorting them out, and replacing the old ones on the shelves all at once.

**Key differences:**

- **Action:** `fetch` downloads, `pull` downloads and merges.
- **Impact:** `fetch` no changes to working files, `pull` updates your working files.
- **Risk:** `fetch` no risk of conflicts, `pull` potential for merge conflicts if local and remote changes clash.
- **Use cases:** `fetch` for previewing changes before merging, `pull` for quick updates and integrating changes directly.

**Remember:**

- Both `fetch` and `pull` are essential for keeping your local repository synchronized with the remote one.
- `fetch` is the safer option when you want to review and plan your integration.
- `pull` is the faster option for quickly merging and incorporating new changes.

## Explain in simple terms git rebase and the command for it

**Imagine you're building a LEGO tower with a friend.** You both have your own sections, but you want to combine them into one awesome tower.

**Merging would be like sticking the two sections together, even if the colors clash a bit.** It works, but it's not super tidy.

**Rebasing would be like carefully taking apart your blocks and rebuilding them on top of your friend's section, making sure everything matches perfectly.** The final tower looks like it was built together from the start!

**Here's the Git command:**

```
git rebase <base-branch>
```

**Replace `<base-branch>` with the name of the branch you want to rebuild on top of.**

**Key points:**

- Rebasing makes a cleaner, neater history, like a perfectly organized LEGO tower.
- Use it with caution on shared towers (branches) so you don't mess up other people's blocks.
- It's great for tidying up your own blocks before sharing them.

## Explain in simple terms git cherry-pick and the command for it

**Imagine Git commits as delicious cherries on a tree:**

- Cherry-picking is like plucking a specific, ripe cherry from one branch and carefully grafting it onto another branch, where it can grow and flourish.

**Here's how it works:**

1. **You have multiple branches, each with their own delicious cherries (commits).**
2. **You find a specific cherry on one branch that you want to transplant onto another branch.** Perhaps it's a bug fix, a new feature, or a particularly sweet improvement.
3. **You use the `git cherry-pick` command to pluck that cherry and graft it onto the desired branch.**
4. **The cherry (commit) is copied and added to the new branch as a brand-new commit, with its own unique ID and history.**

**The command is:**

```
git cherry-pick <commit-hash>
```

**Replace `<commit-hash>` with the unique ID of the commit you want to pick.** You can find this hash by running `git log`.

**For example:**

```
git cherry-pick 123abc45
```

**This picks the commit with the hash `123abc45` and adds it to your current branch.**

**Key points:**

- Cherry-picking is precise: It only copies the selected commit, not its entire history.
- It's great for transferring specific changes between branches without merging entire branches.
- It can help you introduce bug fixes or features without disrupting other work in progress.
- It's like having a cherry picker to pluck the perfect cherries from different trees and create your perfect orchard!
