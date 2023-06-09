# Checkpoint2 Submission

[`checkpoint 2`](https://github.com/0245861155-myseneca/CSN400-Capstone/tree/main/checkpoint2 "Checkpoint 2 github")

# Part A 

- **COURSE INFORMATION: CSN 400 NBB**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER ID: 0245861155-myseneca**
- **TEACHER’S NAME: Atoosa Nasiri**

# Table of contents 

1. [Part A](#part-a)
2. [Part B - results of Git Status and Git Log](#part-b)
3. [part C - creating and Merging branches](#part-c)
4. [part D - Git Branching questions](#part-d)

# PART B

### what is `git log` and `git status`

### The `git status` command provides an overview of the current state of files in your working directory and staging area, highlighting which files have been modified, added, or deleted. On the other hand, the `git log` command displays a chronological list of commit history, including commit messages, authorship, dates, and unique identifiers for each commit.

## part C

### Footnotes Folder created

### results of git `log -n 5`

```bash

# tjkir@TylerK-1 MINGW64 /g/Semester 5/OPS 445 NBB/Sriptes/CSN400-Capstone/checkpoint2 (main)
$ git log -n 5
commit bc1qre8jdw2azrg6tf49wmp652w00xltddxmpk98xp (HEAD -> main, origin/feat-emojies, feat-emojies)
Author: Tyler Kirkwood <tkirkwood@myseneca.ca>
Date:   Mon May 15 19:52:18 2023 -0400

    adds emojies to feat-emojis branch

commit a5ecfd37efc6d4c80cb964091185ad9dd1624357 (origin/main, origin/HEAD)
Author: Tyler Kirkwood <tkirkwood@myseneca.ca>
Date:   Mon May 15 19:46:25 2023 -0400

    adds footnotes folder

commit 8a6f2944d35dbe70550afda98688ef7e458be51d
Author: Tyler Kirkwood <tkirkwood@myseneca.ca>
Date:   Mon May 15 19:44:41 2023 -0400

    Update for status and footnotes folder

commit be48cb6ffecd486a41eda9a534002a1a4e6f32e9
Author: Tyler Kirkwood <tkirkwood@myseneca.ca>
Date:   Mon May 15 11:35:43 2023 -0400

    Added course information

commit a1d6e6b3ce894b826b33298f1a169309463f4ef9
Author: Tyler Kirkwood <tkirkwood@myseneca.ca>
Date:   Mon May 15 10:31:55 2023 -0400

    Checkpoint 2

tjkir@TylerK-1 MINGW64 /g/Semester 5/OPS 445 NBB/Sriptes/CSN400-Capstone/checkpoint2 (main)

``` 

# part D

### `1.` What are the differences between develop branch and main branch?

#### `A.` The main branch is considered to be the primary branch where code is branched off from and merged to anything in the main branch is deployable. The develop branch is a stable branch for developers. It’s where new features, functions, and major changes are worked on in separate feature branches. These feature branches are created from the develop branch and then merged back into it once the work is completed.

### `2.` What are the three supporting branches? Briefly describe the function of each of these supporting branches.

#### `A.` `Feature` branches are used for devopling new features or major changes
#### `A.` `Release`  branches are created when enough features have accumulated or the next release time frame comes near
#### `A.` `Hotfix` branches are use to quicly repair major problems found after the release

### `3.` What are the best practices in working with release branches?

#### `A.` Some best practices for release branches include creating them close to the actual release, applying changes to both the release and main branches, and merging changes from earlier versions. Release branching is important for supporting versioned software and changes in earlier versions may need to be merged to later release branches.

