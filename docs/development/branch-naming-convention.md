---
sidebar_label: Branch Naming Convention
sidebar_position: 4
---

# Branch Naming Convention

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-006-v1
</code>
<br></br>
Branches should contain the issue id if the work is related to an issue.
<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-007-v1
</code>
<br></br>
Branches should contain the <a href="#branch-types">Branch Type</a>, such as `feat`, `fix` or `chore`
<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-STD-008-v1
</code>
<br></br>
Branches should be named in kebab-case.
<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-STD-009-v1
</code>
<br></br>
Do not use the <a href="#examples">Reserved branch names</a> for branches.

<br></br>
<br></br>

Check out all the rules in the <a href="/auditing/rules">Auditor Rules</a> section.
:::

:::info
This guide is mainly focused on working on GitHub, but the same principles can be applied to other Git hosting services.
:::

In this guide, we will outline the standard procedures and guidelines for naming Git branches within our software development workflow. Good naming conventions are essential for team collaboration and project management.


## Purpose

The primary purposes of having a proper naming convention for Git branches are to maintain organization, ease of access, and understanding the purpose of different branches.

## Naming Git Branches

### Non-Issue-related Branches

All git branches that aren't directly associated with an issue should follow the following naming conventions:

`<type>/<name>`
- `<type>` - The type of branch. See [Branch Types](#branch-types) for more information.
- `<name>` - A brief description of the work the branch involves. See [Branch Names](#branch-names) for more information.

:::tip
We recommend not using non-issue-related branches. Instead, create an issue for the work you want to do, and then create a branch related to that issue. This will help keep track of the progress of the work and will make it easier to understand the purpose of the branch.
:::


### Issue-related Branches

Branches related with a specific issue should contain the issue number and a brief description of the work involved. Here is the format:
This is useful for tracking the progress of the issue and for understanding the purpose of the branch.
Some issues trackers (such as GitHub) will automatically link the branch to the issue if the branch name contains the issue number.

`<type>/<issue-number>-<name>`

- `<type>` - The type of branch. See [Branch Types](#branch-types) for more information.
- `<issue-number>` - The issue number associated with the branch.
- `<name>` - A brief description of the work the branch involves. See [Branch Names](#branch-names) for more information.

### Branch Types

- Feature branches: `feat` These branches are used to add new features to the project.
- Bug fix branches: `fix` These branches are used to fix bugs in the project.
- Refactoring branches: `refactor` These branches are used to refactor code in the project.
- Experimental branches: `exp` These branches are used to experiment with new ideas.
- Maintenance branches: `chore` These branches are used to perform general maintenance on the project.

:::info
Chore branches are usually not associated with an issue. They are used for general maintenance tasks such as updating dependencies or fixing repository related issues.
:::

### Branch Names

The name of the branch should be a brief description of the work the branch involves. It should be descriptive enough to give a quick idea about what changes the branch introduces.

- The name should be all lower case.
- Use hyphens `-` to separate words in the name, not spaces or underscores.
- The name should be brief but descriptive.
- It should give a quick idea about what changes the branch introduces.
- Avoid using generic names such as `update` or `fix`.

## Examples

- `feat/1234-red-button` - A feature branch that adds a red button. The issue number is 1234.
- `fix/1234-missing-button` - A bug fix branch that fixes a missing button. The issue number is 1234.
- `refactor/1234-button-component` - A refactoring branch that refactors the button component. The issue number is 1234.
- `chore/update-dependencies` - A maintenance branch that updates the dependencies. This branch is not associated with an issue.
- `exp/new-button` - An experimental branch that experiments with a new button. This branch is not associated with an issue.

:::danger Reserved Branch Names

Some branch names are reserved for specific purposes. These branches should not be used for any other purpose.

- `master` - The main branch of the repository. This branch should contain the latest stable version of the project.
- `develop` - The development branch of the repository. This branch should contain the latest development version of the project.
- `release` - The release branch of the repository. This branch should contain the latest release version of the project.
- `hotfix` - The hotfix branch of the repository. This branch should contain the latest hotfix version of the project.

:::


## Conclusion

Adhering to these branch naming conventions will result in a cleaner and more structured codebase, leading to an improved collaborative environment. It will ensure that all team members can easily understand what work is being carried out on a particular branch.

Remember, consistency is the key. The more consistent we are, the more efficient and effective our workflow will be.
