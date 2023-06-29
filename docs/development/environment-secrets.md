---
sidebar_position: 10
---

# Environment Secrets

:::note Auditing

In this document the following auditing rules are covered:

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-SEC-024-v1
</code>
<br></br>
Environment secrets should not be hardcoded in the source code.

<br></br>

<code style={{backgroundColor:'#1abc9c', color: 'white', paddingLeft:10, paddingRight: 10}}>
DEV-SEC-025-v1
</code>
<br></br>
Environment secrets should be stored in a secure location such as a secret management system or encrypted file.

<br></br>
<br></br>

Check out all the rules in the [Auditor Rules](/auditing/rules) section.
:::



Environment secrets are sensitive data that are used in the configuration of applications. They can be API keys, database usernames and passwords, encryption keys, OAuth tokens, and other types of credentials that your application needs to function.

Environment secrets are often stored in the environment variables of the host machine where the application is running. However, they can also be stored in other secure locations such as secret management systems or encrypted files, and accessed by the application at runtime.

### Importance of Environment Secrets

Environment secrets are pivotal for various reasons:

- **Security**: Environment secrets are a necessary evil in the world of computing. They grant your applications the necessary permissions to interact with other systems and services.
- **Functionality**: Many services rely on secrets for functionality. For example, an application might need an API key to interact with a third-party service, or a database password to fetch data from a database.

### Why You Should Not Hardcode Environment Secrets

Hardcoding environment secrets directly into your code can lead to several severe issues:

- **Security Risks**: If your code, along with the hardcoded secrets, ends up in a public repository, anyone can see and misuse them. Even within private repositories, it's a best practice to not include sensitive data, as it's hard to control and monitor who has access.
- **Lack of Flexibility**: If secrets are hardcoded, they can't be easily changed or rotated. Regular rotation of secrets is a standard security practice.
- **Operational Issues**: Different environments (development, testing, production) often require different sets of secrets. Hardcoding secrets makes it hard to manage these different sets and can lead to operational difficulties.

### Best Practices for Managing Environment Secrets

Considering the security risks of hardcoding environment secrets, the following best practices can be employed to manage them effectively:

- **Secret Management Tools**: Use tools such as HashiCorp Vault, AWS Secrets Manager, or Azure Key Vault. These tools store secrets securely and provide access control to ensure only authorized applications and users can access the secrets.
- **Environment Variables**: You can also store secrets in environment variables, but you should ensure that these variables are not exposed in any logs or error messages. Furthermore, never include them in your source code or version control systems.
- **Use .env files with Caution**: If you're storing secrets in .env files, ensure these files are added to your .gitignore or equivalent file, to prevent them from being uploaded to your source control.
- **CI/CD Pipeline**: Most CI/CD tools provide ways to securely inject secrets into your applications at deployment time. These secrets are encrypted and can be securely managed.
- **Regularly Rotate Secrets**: Regularly change your secrets to mitigate the risk in case they are compromised. Automated secret rotation is a feature of many secret management tools.

[//]: # (TODO: integrate https://github.com/awslabs/git-secrets into the guide)
