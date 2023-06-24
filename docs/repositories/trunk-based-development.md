---
id: trunk-based-development
sidebar_position: 2
---

# Trunk-Based Development

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-007-v1
</code>
<br></br>
Default branch name should be either `master` or `main`.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-009-v1
</code>
<br></br>
Releases should be tagged using a semantic versioning scheme.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-010-v1
</code>
<br></br>
The default branch should be protected from direct pushes.

<br></br>
<br></br>

Check out all the rules in the <a href="/auditor/rules">Auditor Rules</a> section.
:::


## What is Trunk-Based Development?
Trunk-based development (TBD) is a source control workflow model that enables continuous integration.

The primary purpose of trunk-based development is to avoid the creation of long-lived branches by merging partial changes to the entire feature. Developers can achieve this by committing straight to the main branch or by using short-lived branches with an efficient code review process. Branches, by definition, should only live a few days.

If other developers are working on related changes, merging partial changes results in initial feedback, decreases merging complexity, and reduces redundant effort. When the merging process is efficient, the developer does not lose focus by going back and forth between tasks. Because the main branch, also known as the trunk, should be ready to deploy at any time, each modification should not break the build. There are procedures, such as automated testing, feature flags, and branching by abstraction, that enable the team to adopt this methodology.

Benefits of using trunk-based development
1. Complexity is reduced: One of the primary advantages of trunk-based development is the reduced complexity of merging multiple branches into one. This method aims to avoid merge hell, a circumstance in which separate components must be integrated for the first time, resulting in unforeseen bugs, integration challenges, and preventing the team from deploying.

2. Speed of delivery is increased: Implementing and using trunk-based development in the long term could increase team discipline and a feeling of teamwork by establishing clear processes and giving more opportunities for collaboration. According to a Google research, high-performing firms are more likely to use trunk-based development.

3. Feedback loop is shortened: Short feedback loops might also assist validate early design assumptions. Because the trunk should be always stable, the code is potentially releasable to customers for getting early feedback.


```mermaid
%%{init: { 'logLevel': 'debug', 'theme': 'base', 'gitGraph': {'showBranches': true, 'showCommitLabel':false,'mainBranchName': 'master','mainBranchOrder': 2}} }%%
gitGraph
   commit tag:"1.0.0"
   commit
   branch feature/235-add-search-bar order: 3
   checkout feature/235-add-search-bar
   commit
   commit
   checkout master
   merge feature/235-add-search-bar
   commit
   branch fix/764-fix-profile-update order: 4
   checkout fix/764-fix-profile-update
   commit
   commit
   checkout master
   merge fix/764-fix-profile-update
   commit tag:"1.0.1"
```
