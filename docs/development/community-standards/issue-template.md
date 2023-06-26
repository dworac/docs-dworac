---
id: issue-templates
---

# Issue Templates

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-015-v1
</code>
<br></br>
A template for bug reports should be present in the repository with the path <code>.github/ISSUE_TEMPLATE/bug_report.md</code>.
<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-016-v1
</code>
<br></br>
A template for feature requests should be present in the repository with the path <code>.github/ISSUE_TEMPLATE/feature_request.md</code>.
<br></br>

<br></br>
<br></br>

Check out all the rules in the <a href="/auditor/rules">Auditor Rules</a> section.
:::


Issue templates, such as `ISSUE_TEMPLATE.md`, are vital components for managing software repositories. They help standardize the way users submit issues—bugs, feature requests, or any other types of reports. This standardization makes it easier for project maintainers to understand and address these issues.

Issue templates are typically located in the repository's `.github/ISSUE_TEMPLATE` directory. They should be named to reflect their purpose (e.g., `bug_report.md`, `feature_request.md`) and should be written in Markdown.

An example of a bug report template might look like this:

```markdown title="/.github/ISSUE_TEMPLATE/bug_report.md"
---
name: Bug report
about: Create a report to help us improve
title: ''
labels: 'bug'
assignees: ''

---

**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Desktop (please complete the following information):**
 - OS: [e.g. iOS]
 - Browser [e.g. chrome, safari]
 - Version [e.g. 22]

**Additional context**
Add any other context about the problem here.
```

An example of a feature request template might look like this:

```markdown title="/.github/ISSUE_TEMPLATE/feature_request.md"
---
name: Feature request
about: Suggest an idea for this project
title: ''
labels: 'enhancement'
assignees: ''

---

**Is your feature request related to a problem? Please describe.**
A clear and concise description of what the problem is. Ex. I'm always frustrated when [...]

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.
```

:::tip
Explicit Instructions: Be clear and explicit about the information you need for each type of issue.
:::

:::caution
Flexibility: Different issues may require different kinds of information. Make sure your templates are flexible enough to handle a variety of situations.
:::

## Why?

Having well-structured Issue templates can:

- Improve Quality: It helps maintain the quality of reported issues by guiding reporters to include all the necessary information.

- Increase Efficiency: It saves maintainers' time by preventing them from having to ask for more details on reported issues.

- Provide Consistency: It makes all reported issues consistent, facilitating their management and resolution.

## What?

A typical Issue template might include:

- Description: A brief description of the issue.

- Steps to Reproduce: For a bug report, a step-by-step explanation of how to reproduce the issue.

- Expected Behavior: An explanation of what was expected to happen.

- Actual Behavior: An explanation of what actually happened.

- Screenshots: If applicable, reporters can add screenshots to help explain the problem.

- Environment: Details about the environment in which the issue occurred, such as operating system, browser version, etc.

## How?

- Markdown: The Issue template is written in Markdown, a lightweight markup language that's easy to read and write. It's used to format text on GitHub and other platforms. For more information on Markdown, see the [Markdown Guide](https://www.markdownguide.org/).

- Direct and Precise - Direct and Precise: Ensure your templates are clear and instructive. The reporter should easily understand what information is needed in each section.

- Use GitHub's Functionality: GitHub allows you to set default labels, assignees, and more when creating issue templates. This can help automate some aspects of issue management.

## Conclusion

Issue templates are a fundamental part of effective project management. They help ensure consistency, completeness, and clarity in issue reporting, making it easier for maintainers to understand and resolve these issues. Tailoring your issue templates to your project's needs can greatly enhance the contribution and maintenance processes of your project.
