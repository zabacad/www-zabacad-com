---
title: Remembering ls and tar arguments
categories:
    - operations
tags:
    - ls
    - tar
    - remembering

---
Most shell commands follow the same pattern.

```bash
command [-o|--options] file [file] ...
```

The files tail the options. Some commands allow seperation of these file lists with `--` for unambiguity.

```bash
git checkout -- file
```

It gets confusing when there are multiple files involved. In such cases, it helps to pick out the single unique file. Generally:

- The file that already exists when the other do not.
- The file that does not exist when the others do.

Here are some examples, with the less unique files trailing and separated by some extra space:

```bash
ln -s new_link  existing_file
tar -cf new_archive  added_file_1 added_file_2
tar -xf existing_archive
gcc -o new_program  source_1.c source_2.c
```

Many commands allow the files to come before the options, but I like to make a habit of trailing the files.
