---
id: security-policy
---

# Security Policy

:::caution
Not having a security policy will result in the repository being flagged by the Auditor with the rule code:

`DEV-DOC-006-v1`
:::

The SECURITY.md file is an important aspect of any software repository. It provides a way for project maintainers to communicate to users how they handle security vulnerabilities in the project. This can include information about how to report a security vulnerability, what to expect when a vulnerability is reported, and any known security vulnerabilities and their fixes.

The SECURITY.md file should be located in the root directory of the repository or in the `.github` directory. It should be named `SECURITY.md` and should be written in Markdown.

```markdown title="/SECURITY.md"
# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability within this project, please send an email to [Your Email]. All security vulnerabilities will be promptly addressed.

....
```

:::tip
Maintain Transparency: Being transparent about your security policy helps users trust your software. Be clear and upfront about what users should expect when a security vulnerability is reported.
:::

:::caution
Sensitive Information: Do not disclose sensitive details of the vulnerability publicly until it has been addressed.
:::

## Why?

The SECURITY.md file is crucial for maintaining the security of a software project.

- User Safety: It gives users clear instructions on how to report potential security issues, contributing to the overall safety and integrity of the project.

- Efficient Resolution: By directing security reports to the appropriate channel, issues can be addressed more efficiently.

- Transparency: It communicates to users that the project takes security seriously, and there is a protocol in place to handle vulnerabilities.

## What?

A typical SECURITY.md file contains the following sections:

- Supported Versions: List which versions of the project are currently being supported with security updates.

- Reporting a Vulnerability: Provide instructions on how to report a security vulnerability. This often includes the process, expectations, and a method of contact.

- Disclosure Policy: Outline your policy on how the disclosure of security vulnerabilities is handled.

- Comments on Security: Any additional information that users might find useful, such as common security issues and how to prevent them.

:::tip
Direct Communication: Directing security vulnerabilities to a specific email or a private issue tracker can help prevent the details of the vulnerability from being disclosed publicly before you've had a chance to address it.
:::

## How?

- Markdown: The SECURITY.md file is written in Markdown, a lightweight markup language that's easy to read and write. It's used to format text on GitHub and many other platforms. For more information on Markdown, see the [Markdown Guide](https://www.markdownguide.org/).

- Clarity: When writing a SECURITY.md file, it is important to be clear and precise. Users need to know exactly what to do if they discover a security vulnerability.

- Updates: Make sure the SECURITY.md file is kept up-to-date. If your security policy or contact details change, ensure that they are updated in the SECURITY.md file.

## Conclusion

A SECURITY.md file is an important part of any software project, as it outlines the project's policy for handling security vulnerabilities. By providing clear instructions for reporting vulnerabilities, and by outlining the procedures for handling such reports, a SECURITY.md file can help maintain the security and integrity of a project.
