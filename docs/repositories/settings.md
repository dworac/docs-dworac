---
sidebar_label: Settings
sidebar_position: 4
---

# Repository Settings Probot App

This guide aims to outline the standard procedures and guidelines for utilizing the Repository Settings Probot App in our software development workflow. Properly configuring and understanding this app is essential for enhancing our team collaboration and project management.

:::caution
Incorrect configurations may disrupt the repository settings and thus hamper your workflow. Ensure to follow the guide meticulously.
:::

## Purpose

The primary purpose of the Repository Settings Probot App is to synchronize the repository settings defined in `.github/settings.yml` with GitHub. It allows the initiation of Pull Requests for modifying repository settings, thus enhancing project management.

## Using Repository Settings Probot App

### Steps

1. __[Install the app](https://github.com/apps/settings)__ to your GitHub account.
2. Create a `.github/settings.yml` file in your repository. Any changes made to this file on the default branch will be synced to GitHub.

:::tip
You can define multiple settings in the `.github/settings.yml` file like the repository name, description, access permissions, branch protections, and many more. For detailed information on all available settings, refer to the [GitHub API documentation](https://docs.github.com/en/rest/reference/repos#update-a-repository).
:::

### Sample `.github/settings.yml` Configuration

```yaml title=".github/settings.yml"
# These settings are synced to GitHub by https://probot.github.io/apps/settings/

repository:
  # See https://docs.github.com/en/rest/reference/repos#update-a-repository for all available settings.

  # The name of the repository. Changing this will rename the repository
  name: docs

  # A short description of the repository that will show up on GitHub
  description: Documentation for dworac organization. Basic guidelines for projects, tools and others.

  # Either 'true' or 'false' to make it a template.
  is_template: false

  # A URL with more information about the repository
  homepage: https://docs.dworac.com/

  # A comma-separated list of topics to set on the repository
  topics: dworac,docs,documentation,github,organization

  # Either `true` to make the repository private, or `false` to make it public.
  private: false

  # Either `true` to enable issues for this repository, `false` to disable them.
  has_issues: true

  # Either `true` to enable projects for this repository, or `false` to disable them.
  # If projects are disabled for the organization, passing `true` will cause an API error.
  has_projects: false

  # Either `true` to enable the wiki for this repository, `false` to disable it.
  has_wiki: false

  # Either `true` to enable downloads for this repository, `false` to disable them.
  has_downloads: true

  # Updates the default branch for this repository.
  default_branch: master

  # Either `true` to allow squash-merging pull requests, or `false` to prevent
  # squash-merging.
  allow_squash_merge: false

  # Either `true` to allow merging pull requests with a merge commit, or `false`
  # to prevent merging pull requests with merge commits.
  allow_merge_commit: true

  # Either `true` to allow rebase-merging pull requests, or `false` to prevent
  # rebase-merging.
  allow_rebase_merge: true

  # Either `true` to enable automatic deletion of branches on merge, or `false` to disable
  delete_branch_on_merge: true

  # Either `true` to enable automated security fixes, or `false` to disable
  # automated security fixes.
  enable_automated_security_fixes: true

  # Either `true` to enable vulnerability alerts, or `false` to disable
  # vulnerability alerts.
  enable_vulnerability_alerts: true

branches:
  - name: master
    # https://docs.github.com/en/rest/reference/repos#update-branch-protection
    # Branch Protection settings. Set to null to disable
    protection:
      # Required. Require at least one approving review on a pull request, before merging. Set to null to disable.
      required_pull_request_reviews:
        # The number of approvals required. (1-6)
        required_approving_review_count: 0
        # Dismiss approved reviews automatically when a new commit is pushed.
        dismiss_stale_reviews: false
        # Blocks merge until code owners have reviewed.
        require_code_owner_reviews: true
      # Required. Require status checks to pass before merging. Set to null to disable
      required_status_checks:
        # Required. Require branches to be up to date before merging.
        strict: false
        # Required. The list of status checks to require in order to merge into this branch
        contexts: []
      # Required. Enforce all configured restrictions for administrators. Set to true to enforce required status checks for repository administrators. Set to null to disable.
      enforce_admins: true
      # Prevent merge commits from being pushed to matching branches
      required_linear_history: false
      # Required. Restrict who can push to this branch. Team and user restrictions are only available for organization-owned repositories. Set to null to disable.
      restrictions: null
```

:::info
The `settings.yml` file is written in YAML. It's a strict superset of JSON, with the addition of syntactically significant newlines and indentation, like Python. For more information, refer to the [YAML documentation](https://yaml.org/).
:::

## Security Implications
:::warning
Note that this app inherently escalates anyone with push permissions to the admin role, since they can push config settings to the master branch, which will be synced. Use caution when merging PRs and adding collaborators.
:::

One way to preserve admin/push permissions is to utilize the GitHub CodeOwners feature to set one or more administrative users as the code owner of the .github/settings.yml file, and turn on "require code owner review" for the master branch. This does have the side effect of requiring code owner review for the entire branch, but helps preserve permission levels.

In order to turn on required code owner review for the master branch, you can use the following settings:

```yaml title=".github/settings.yml"
branches:
  - name: master
    protection:
      required_pull_request_reviews:
        require_code_owner_reviews: true
```

And add the following to the bottom of the .github/CODEOWNERS file: (replace `@dworac` with the GitHub username of the admin user)

``` yaml title=".github/CODEOWNERS"
.github/settings.yml @dworac
```

This will require code owner review for any changes to the .github/settings.yml file, but not for any other files in the repository. If anyone wants to make changes to the settings, they will need to create a PR and have it approved by the code owner before it can be merged.


