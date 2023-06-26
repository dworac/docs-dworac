---
id: changelog
sidebar_position: 7
---

# Changelog

:::note Auditing
In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-021-v1
</code>
<br></br>
A changelog should be present in the repository's root directory.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-DOC-022-v1
</code>
<br></br>
The changelog should be automatically generated using a tool such as <a href="#automating-with-release-please">Release Please</a>

<br></br>
<br></br>

Check out all the rules in the <a href="/auditor/rules">Auditor Rules</a> section.
:::

The CHANGELOG.md file is a vital part of any software repository. It offers a concise, chronological summary of all the significant changes made to each version of a project. This can include details about new features, bug fixes, deprecated functionalities, and any other notable modifications.

The CHANGELOG.md file should be located in the root directory of the repository. It should be named `CHANGELOG.md` and should be written in Markdown.

```markdown title="/CHANGELOG.md"
# Changelog

## [1.0.1] - 2023-06-19

### Added

- Feature: Added support for XYZ

### Fixed

- Bug: Fixed issue with ABC

....
```

:::tip
Maintain Transparency: Being open about your project changes helps users understand your software's evolution and anticipate potential issues. Be clear and comprehensive about what users should expect in each version.
:::

:::caution
Consistency: Ensure consistency in the formatting and language of your CHANGELOG for easy comprehension.
:::

## Why?

The CHANGELOG.md file is crucial for maintaining transparency and understanding in a software project.

- User Awareness: It provides users with a detailed list of changes, helping them understand what has been improved, fixed, or altered in the project.

- Easy Troubleshooting: By documenting the changes, users can easily associate issues they are facing with a specific release.

- Transparency: It communicates to users that the project is actively maintained and improved, promoting trust in the software.

## What?

A typical CHANGELOG.md file contains the following sections for each version:

- Release Version and Date: The version of the release and the date it was released.

- Added: Details of any new features or enhancements added.

- Changed: Details of any changes made to existing functionality.

- Deprecated: Details of any features or functionalities that are no longer in active development or use.

- Removed: Details of any features or functionalities that have been removed.

- Fixed: Details of any bugs or issues that have been resolved.

:::tip
Semantic Versioning: Using a versioning system like [Semantic Versioning](https://semver.org/) can provide a clear and standardized understanding of how the software is evolving.
:::

## How?

- Markdown: The CHANGELOG.md file is written in Markdown, a lightweight markup language that's easy to read and write. It's used to format text on GitHub and many other platforms. For more information on Markdown, see the [Markdown Guide](https://www.markdownguide.org/).

- Clarity: When writing a CHANGELOG.md file, it is essential to be clear and precise. Users need to know exactly what has changed in each release.

- Updates: Make sure the CHANGELOG.md file is updated with each new release. If a new feature is added or an old bug is fixed, ensure that it is documented in the CHANGELOG.md file.

## Automating with Release Please

Release please is a GitHub Action that automatically generates a CHANGELOG.md file based on the commit history of a repository. It also creates a new release and tags it with the version number. For more information on Release Please, see the [Release Please GitHub Action](https://github.com/google-github-actions/release-please-action)

In order to setup Release Please, you need to create a `.github/release-please.yml` file in the root directory of your repository. 

```yaml title="/.github/release-please.yml"
name: Release Please
permissions:
  contents: write
  pull-requests: write
on:
  push:
    branches:
      - master
jobs:
  release-please:
    runs-on: ubuntu-latest
    steps:
      - uses: google-github-actions/release-please-action@v3
        id: release
        with:
          release-type: node
          package-name: release-please-action
          token: ${{ secrets.MY_TOKEN }}
```

Whenever a new commit is pushed to the master branch, Release Please will automatically generate a new Pull Request with the updated CHANGELOG.md file. Once the Pull Request is merged, Release Please will create a new release and tag it with the version number.

This is useful for maintaining a consistent and up-to-date CHANGELOG.md file. It also helps automate the release process, saving time and effort.

:::tip
Make sure to use commit messages that follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format. This will help Release Please generate a more accurate CHANGELOG.md file.
:::

:::caution
Be sure to add MY_TOKEN to your repository secrets. This will allow Release Please to access your repository and create new releases.
:::

## Conclusion

A CHANGELOG.md file is an essential part of any software project, as it tracks the evolution of the project over time. By offering a clear summary of changes for each release, a CHANGELOG.md file can keep users informed and help maintain transparency in the project.
