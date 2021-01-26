---
description: Common git commands and their applications are introduced here.
---

# Git Commands & GitHub

## What is Git?

**Git** is a **distributed version-control system** for tracking changes in any set of files, originally designed for coordinating work among programmers cooperating on source code during software development. Its goals include speed, data integrity, and support for distributed, non-linear workflows. - [Wikipedia](https://wiki2.org/en/Git)

Simply put, Git helps users for tracking different versions of the software and easily to reverting back between versions in case of unexpected results - instead of creating multiple copies of the files \(for each version\) multiple times and renaming them.

**Git** is the distributed version-control system whereas **GitHub** is a repository hosting service. You need to install Git to use on your computer and it doesn't require internet connection unlike GitHub in which you own / share repositories on the web to work on your projects. 

![Data flows and Storage levels in the Git revision control system](../../.gitbook/assets/git-operations.png)

### Installing & Updating Git

There are multiple options to install Git to your computer. First, open a terminal and check if Git is installed already and if so find the version of Git typing the command below:

```bash
>>> $ git version
git version 2.28.0 # 2nd major, 28th minor and 0th patch version
```

Since it is already install in my local computer, the command prints the version of current git install. 

If Git is already installed, you can download the latest development version via Git by cloning the git [repository](https://github.com/git/git) or simply upgrade using brew \(in MacOS in my case\).

```bash
# clone the latest repo
>>> git clone https://github.com/git/git

# or upgrade the version
>>> brew upgrade git
```

If it is your first time, you can download your preferred version of Git from [here](https://git-scm.com/downloads) and install it using the package installer. Follow the link for other options to install Git.

