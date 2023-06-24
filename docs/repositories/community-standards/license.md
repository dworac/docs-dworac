---
id: license
---

# License

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-007-v1
</code>
<br></br>
A License should be present in the repository's root directory with the name <code>LICENSE</code>.

<br></br>
<br></br>

Check out all the rules in the <a href="/auditor/rules">Auditor Rules</a> section.
:::


The LICENSE file is an important part of any software repository. It describes the conditions under which the software can be used and distributed, as well as the responsibilities and liabilities of the user.

The LICENSE file should be located in the root directory of the repository. It should be named `LICENSE` or `LICENSE.txt` and could be written in plain text or Markdown.

```text title="/LICENSE"
MIT License

Copyright (c) [year] [fullname]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
....
```

:::tip
Choose Appropriate License: When choosing a license for your project, it's important to understand the implications of the different licenses available. You can use resources like [Choose a License](https://choosealicense.com/) to help make an informed decision.
:::

:::caution
Do Not Alter Licenses: Licenses are legal documents. Altering the text of a license may change its meaning, so it's generally recommended not to modify the text of an existing license without legal advice.
:::

## Why?

Including a LICENSE file in your project repository is not just a matter of legal compliance; it also communicates to users and contributors the terms under which they can use, modify, or distribute your software.

- Legal Compliance: If you want others to use your software, it's essential to specify a license that outlines the terms and conditions of use. Without a license, others may not legally use your software.

- Clarity: A license provides clarity about the permissions given to others regarding the use, modification, and distribution of your project.

- Open Source: If you want your project to be considered open source, it must include a license that complies with the Open Source Definition.

## What?

A typical LICENSE file includes:

- The name and version of the license.
- The full text of the license, including permissions, conditions, and limitations.
- The year and the name of the copyright holder (usually the author or the organization).

## How?

- Text or Markdown: The LICENSE file is typically written in plain text or Markdown. This ensures that it can be read in any text editor, and on any operating system.

- Formatting: As legal documents, licenses should be presented as they are without any additional formatting or changes. Each license usually has its own specific formatting.

- Attribution: The LICENSE file should include the correct copyright attribution, usually including the year and the name of the copyright holder. The copyright holder is generally the person or organization who created the work.

:::tip
Use a Template: Many open-source licenses are available as ready-to-use templates, such as the MIT License or the GNU General Public License. These templates include the full text of the license, and usually only require you to add your name and the current year.
:::

## Conclusion

In conclusion, a LICENSE file is a vital part of any software project, providing clear instructions about how the software can be used, modified, or distributed. It's important to select a license that aligns with your goals for the project, and to include the license in a clearly labeled file in the root of your project repository.
