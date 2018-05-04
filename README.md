# What is Git ?
A Software that helps in keeping track of changes to your project / files / directory. 
- Especially _text changes_
- Helps you move back and forward between versions / changes _(version 1, version 2, version 3)_
- referred to as a **Version Control System (VCS)**
- 90-95% of the time VCS are used for **Source Code Management (SCM)**
-  Comes as built in / as a plugin in almost (if not all) Editors / IDEs.

---

### Examples of Version Control (non-source code)
- File naming (Budget_v4.xls, Logo_v2.gif)
- Microsoft word's track changes / Sharepoint
- Adobe Photoshop's _History_
- Wiki's _versioning / rollbacks_
- Undo: `Ctrl + Z` (Win) or `Cmd + Z` (Mac)

---

# VCS other than Git ...
- `Source Code Control System (SCCS)`
	- 1972, closed / proprietary, free with Unix
	- Most basic form of versioning
	- Just save the snapshot of the document
	- Keeps the **original file** as reference, maintains track of changes
	- Keeps track of a single file only, not a whole set / directory
- `Revision Control System (RCS)`
	- 1982, Cross platform
	- Keeps the **latest file** as reference, previous version to chain
	- Faster - each version only knows it's prev and next
	- Keeps track of a single file only, not a whole set / directory
- `Concurrent Versions System (CVS)`
	- 1986 - 1990, Open source
	- Keeps track of more than one file / the entire directory
	- First to introduce a `Repository` - Remote / Local, hence the name ...
	- More than one developer, can work on a project, `concurrently`
- `Apache Subversion (SVN)`
	- 2000, Open Source - Apache _(duh)_
	- Keep tracks of not only Text file (.txt), BUT even images (.jpg, .png, .jpeg, .gif .....) (unlike any previous tools...)
	- Can keep track of `History` of directories (like file name changes)
		- CVS, had a hard time to track history - If file name ever got changed
	- It's watching a Directory as a whole (and all changes under it)
	- SNAPSHOT is bigger than other tools.
- `Bitkeeper SCM`
	- 2000, closed, proprietary (Community version was free... but only source code for Linux kernel)
	- Distributed Version Control  - New concept unlike other tools
	- BUT in April 2005, all version was CLOSED / proprietary
- `Git is born` 
	- April 2005, by Linus Torvalds (Creator of Linux)
	- Pulled concepts from Bitkeeper
	- Open source and free software, released to Community
	- compatible with Unix, Mac, Solaris
	- Better Safegaurds
	- 100% faster than other VCS (proven .... :O)
	- 2008, Git launched Github (Git repository )
	- 2009, over 50,000 repos, 100,000 users
	- 2011, over 2 million repos, 1 million users

# What is Distributed Version Control

| Central Repository | Distributed Version Control |
|:----------------------|---------------------------------:|
| All other tools, SVN, CVS, SCCS, RCS ..etc., make use of a Central Repository | Git unlike others, follows a Distributed Version Control |
| All of these four tools, use a **central code repository** model, ie., there is one central place where you store your master copy | Git doesn't work that way, Different users / teams **maintain their own repositories instead of working from a central repo** |
| when you are working, you ALWAYS checkout from master repo | The changes made in **Git** are stored as change sets or patches, and we're focused on tracking changes not the versions of the document |
| So, there is no concept of `forking` or `cloning` in Central Repository | Because it's distributed ... 1) There is no need to communicate with central server 2) Faster 3) No Network access is required 4) No single point insecurity |
| **2 Tree** Architecture - 1) Checkin 2) Checkout | **3 Tree** Architecture - 1) Staged 2) Add 3) Commit

# Git Architecture and Workflow

Git works on a concept called `3 Tree Architecture` 

## Workflow

### Git init
```javascript
git init // Initialize your current folder (add versioning to it)
```
### Git clone

```javascript
git clone [url] . //Either clone a URL to your current folder
```
### Git Fork

> NOTE: This is better explained from `Github`

---
### Git - Add
```javascript
git add . // Add changes made in current folder
```
### Git - Commit
```javascript
git commit -m "Appropriate message describing the change you made"
```
### Git - Stash

```javascript
git stash
```
---
### Git - Diff
> NOTE: The Modern Editors (like Atom, VSCode, IntelliJ ...) have this feature built in
```javascript
git diff
```
### Git - Merge

```javascript
git merge 
```

# Best Practices

- Never Download from a Git repo. Always `Clone` / `Fork`
- Always work with Branches  and not `Tags`
- Always Branch out as soon as git clone / git pull is performed
- Give meaningful - proper highlight Commit messages
- Lastly - but NOT LEAST - Comment your code appropriately 

# Simple Change

- Example of a Git stash

```js
console.log(`Hello World`);
```
