---
sidebar_label: Branch Naming Convention
---

# Branch Naming Convention

## Introduction

Branch naming conventions are crucial in a version control system like Git. They allow a team to stay organized, understand the structure of the work, and navigate the project efficiently. This document outlines the branch naming conventions to be adhered to by our team for a more streamlined, consistent, and productive workflow.

## Branch Naming Conventions

Our branch naming conventions are organized into different categories based on the nature of the work.

**1. Feature Branches**

All new features should be developed on a separate branch. These branches should be named using the following convention:

`feature/<ticket number>-<brief-description>`

Example: `feature/123-add-login-button`

**2. Bug Fixes**

All bug fixes should be developed on a separate branch. These branches should be named using the following convention:

`bugfix/<ticket number>-<brief-description>`

Example: `bugfix/456-fix-navigation-bar`

**3. Hot Fixes**

Hot fixes are urgent changes usually related to production issues. These branches should be named using the following convention:

`hotfix/<ticket number>-<brief-description>`

Example: `hotfix/789-correct-typo-homepage`

**4. Refactor**

Branches created for refactoring code should use the following format:

`refactor/<ticket number>-<brief-description>`

Example: `refactor/321-optimize-image-loading`

**5. Experimental / Research**

Branches created for exploring new ideas or conducting some research should use the following format:

`research/<ticket number>-<brief-description>`

Example: `research/654-implement-dark-mode`

## Rules and Guidelines

- Always use lower case and hyphens for spaces.
- Start the branch name with the type of task to be performed (feature, bugfix, etc.).
- Include the ticket number from the project management tool to link your branch to a specific task.
- Add a brief description about the task, using hyphens for spaces.
- Avoid long branch names; try to keep them under 30 characters.
- Do not use special characters in branch names.
- Delete the branch after merging it into the main branch.

## Conclusion

Adhering to these branch naming conventions will result in a cleaner and more structured codebase, leading to an improved collaborative environment. It will ensure that all team members can easily understand what work is being carried out on a particular branch.

Remember, consistency is the key. The more consistent we are, the more efficient and effective our workflow will be.
