---
title: Empty Git commits
categories:
    - development
tags:
    - git

---
In Git, it is possible create an empty commit. That is, a commit with no diff.

```bash
git commit --allow-emtpy
```

Notably, an emtpy commit still includes:

- A commit message
- Branch information

This makes them useful for creating a remote branch to be populated later, such as by someone else or by some automation.

```bash
git checkout -b config-med
git commit --allow-empty -m "Create branch for medium config."
git push -u origin config-med
```
