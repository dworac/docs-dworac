---
sidebar_position: 9
---

# Environment Variables

:::note
We are particularly talking about Environment Variables, not about Secrets. Secrets are a different topic and should be handled differently.
:::

Environment variables are dynamic "named values" that can affect the way running processes behave on a computer. These variables are part of the environment in which a process runs. For example, a running process can access the values of environment variables to receive configuration information.

### Importance of Environment Variables

Environment variables offer a way to influence the behavior of software on the system without hardcoding that information into the program itself. They have several significant use-cases:

- **Configurations**: Environment variables are commonly used for setting application configurations such as database connection strings, paths to relevant directories, API keys, and more.
- **Portability**: They aid in software portability. By using environment variables, you can run your application on different machines or environments without changing the application's code.

### Why You Should Not Hardcode Environment Variables

Hardcoding environment variables means embedding them directly into your code. This practice can create several issues:

- **Lack of Flexibility**: Hardcoded variables limit flexibility. It becomes challenging to use your software in different environments without modifying the code.
- **Maintenance Issues**: Any changes to hardcoded variables require a code change, recompilation, and redeployment of the software. This can be time-consuming and error-prone.

### Best Practices for Managing Environment Variables

Given the importance of not hardcoding environment variables, here are some best practices for managing them:

- **.env files**: Use .env files to store your environment variables and add .env to your .gitignore file to ensure it doesn't get committed to your repository. You can load these variables at runtime using libraries like 'dotenv' in Node.js.
- **Secret Management Tools**: Use secret management tools such as AWS Secrets Manager, or Azure Key Vault. These tools allow you to centrally manage, access, and distribute application secrets.
- **Environment Variables in CI/CD**: Use the CI/CD pipeline to set up environment variables. Most CI/CD tools provide a secure way to store the environment variables, which are injected at runtime.
- **Environment-specific Config Files**: For different environments (development, staging, production), use different config files that store environment variables. This makes the application flexible and easy to manage across different environments.

### Using env variables in node.js

In node.js you can use the [dotenv](https://www.npmjs.com/package/dotenv) package to load your environment variables from a .env file.

```shell
yarn add dotenv
```

Create a .env file in the root of your project and add your environment variables.

```bash
DB_HOST=localhost
DB_USER=root
DB_PASS=s1mpl3
```

Then in your node.js application you can load the environment variables from the .env file.

```js
require('dotenv').config()
```

Now you can access the environment variables in your application.

```js
const db = require('db')
db.connect({
  host: process.env.DB_HOST,
  username: process.env.DB_USER,
  password: process.env.DB_PASS
})
```

Learn more about [dotenv](https://www.npmjs.com/package/dotenv).


### Using env variables in Net Core

In Net Core you can use the [Microsoft.Extensions.Configuration](https://www.nuget.org/packages/Microsoft.Extensions.Configuration/) package to load your environment variables from a .env file.

```bash
dotnet add package Microsoft.Extensions.Configuration
```

Create a .env file in the root of your project and add your environment variables.

```bash
DB_HOST=localhost
DB_USER=root
DB_PASS=s1mpl3
```

Then in your Net Core application you can load the environment variables from the .env file.

```cs
using Microsoft.Extensions.Configuration;


var builder = new ConfigurationBuilder()
    .AddEnvironmentVariables()
    .AddJsonFile("appsettings.json", optional: true, reloadOnChange: true);

var configuration = builder.Build();
```

Now you can access the environment variables in your application.

```cs
var dbHost = configuration["DB_HOST"];
var dbUser = configuration["DB_USER"];
var dbPass = configuration["DB_PASS"];
```

Learn more about [Microsoft.Extensions.Configuration](https://www.nuget.org/packages/Microsoft.Extensions.Configuration/).
