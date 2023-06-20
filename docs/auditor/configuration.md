---
sidebar_position: 3
--- 

# Configuration

The Auditor can be configured by creating a `.github/dworac-auditor.yml` file in your repository. The configuration file is a YAML file that contains the following fields:

```yml title=".github/dworac-auditor.yml"
rules:
  - guideline: code_of_conduct
    required: true
  - guideline: contribution_guide
    required: true
  - practice: consistent_code_style
    required: true
  - practice: no_deprecated_functions
    required: true
  - security: no_public_secrets
    required: true
```
