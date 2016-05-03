# Questions to ask

1- Why I couldnt change the new york times image.

2- How to pull files from github using Jgithub

protocol: git
websites: github, bitbucket, gitlab, stash

git server

git client:
```
git clone repo-url: https://github.com/username/repoName or git@github.com/user/repoName
# makeing changes in the src/a.js src/b.js
git add src/a.js
git add src/b.js
git commit -m "fix issues in a.js and b.js"
# at this point you have commited one of your changed files to the local repository
git pull 
```

local files  --git-|-add-->  git stage  ---git-|-commit--> local repo  <*---git-|-pull-- remote repo
                                                                         ---git-|-push--*>

1- make a change
2- `git add fileName` to stage
3- `git commit`
4- Syncing local and remote repos
  - remote to local: `git pull`
  - local to remote: `git push
  - Syncing
  - Git automatically merges files if it is possible
  - if it is not possible you will have a 'git conflict' which should be resolved

POSSIBLE TO MERGE:
```javascript

//a.js   original a.js
var a = 1;
var b = 2;
var c = 3;

//a.js   v3
var a = 1;
var b = 22;
var c = 3;

// your friend's a.js
//a.js   v3
var a = 1;
var b = 2;
var c = 3;
var d = 4;

//after auto merge
var a = 1;
var b = 22;
var c = 3;
var d = 4;

```

IMPOSSIBLE TO MERGE:
```javascript

//a.js   original a.js
var a = 1;
var b = 2;
var c = 3;

//a.js   v3
var a = 1;
var b = 22;
var c = 3;

// your friend's a.js
//a.js   v3
var a = 1;
var b = 23;
var c = 3;

//CONFLICT

// You have to resolve conflict

```

## .gitignore file
It helps us ignore files and folder.

## git rejects push sometimes

hint: Updates were rejected because the remote contains work that you do                                                        
hint: not have locally. This is usually caused by another repository pushing                                                    
hint: to the same ref. You may want to first integrate the remote changes                                                       
hint: (e.g., 'git pull ...') before pushing again.                                                                              
hint: See the 'Note about fast-forwards' in 'git push --help' for details. 