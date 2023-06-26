---
id: pr-templates
---

# Pull Request Templates

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-018-v1
</code>
<br></br>
A template for pull requests should be present in the repository with the path <code>.github/PULL_REQUEST_TEMPLATE.md</code>.

<br></br>
<br></br>

Check out all the rules in the <a href="/auditing/rules">Auditor Rules</a> section.
:::

Pull Request templates, often named `PULL_REQUEST_TEMPLATE.md`, are crucial tools in streamlining the contribution process in a software project. They guide contributors to provide necessary information when proposing changes to the codebase. This helps maintainers understand the changes, streamline the review process, and ensure that any new pull requests adhere to the project's contribution guidelines.

A Pull Request template should be located in the repository's root directory, in the `.github` directory, or in the `.github/PULL_REQUEST_TEMPLATE` directory. It should be named `PULL_REQUEST_TEMPLATE.md` and should be written in Markdown.

```markdown title="/.github/PULL_REQUEST_TEMPLATE.md"
# Description

Please include a summary of the changes and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.

Fixes # (issue)

## Type of change

Please delete options that are not relevant.

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] This change requires a documentation update

## How Has This Been Tested?

Please describe the tests that you ran to verify your changes. Provide instructions so we can reproduce. Please also list any relevant details for your test configuration

- [ ] Test A
- [ ] Test B

## Checklist:

- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have added tests that prove my fix is effective or that my feature works
- [ ] New and existing unit tests pass locally with my changes
....
```

:::tip
Ensure Clarity: Be clear and specific about what you require in a pull request. This helps contributors to meet your project's standards and guidelines.
:::

## Why?

A well-structured Pull Request template is valuable for several reasons:

- Quality Control: It helps maintain the quality of contributions by ensuring that all pull requests contain the necessary information.

- Efficiency: It streamlines the review process by making sure all the necessary details are available from the start.

- Consistency: It makes all pull requests consistent, making them easier to create and review.

## What?

A typical Pull Request template might include the following sections:

- Description: A brief description of the changes made and the issue it fixes.

- Type of Change: An enumeration of the types of changes (e.g., Bug Fix, New Feature, Documentation, etc.).

- Tests: An explanation of what tests were run to validate the changes.

- Checklist: A list of items for the contributor to confirm before submitting the pull request.

:::tip
Adapt To Your Project: Tailor your Pull Request template to your project's specific needs. Different types of projects might require different information.
:::

## How?

- Markdown: The Pull Request template is written in Markdown, a lightweight markup language that's easy to read and write. It's used to format text on GitHub and many other platforms. For more information on Markdown, see the [Markdown Guide](https://www.markdownguide.org/).

- Clarity and Detail: Ensure that the template is clear and detailed. Contributors should easily understand what information is required from them.


:::tip 
Use GitHub's Functionality: GitHub allows the use of certain keywords to automatically close issues when the pull request is merged. Use keywords like "closes", "fixes", or "resolves" followed by the issue number to take advantage of this feature.
:::


## Conclusion

In conclusion, a Pull Request template is a vital tool in any software project. It helps ensure that contributions meet the necessary standards, aids in streamlining the review process, and encourages consistency in contributions. By providing clear and detailed templates, you enable contributors to effectively and efficiently propose changes to your project.
