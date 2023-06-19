---
sidebar_label: Naming Convention
sidebar_position: 2
---

# Repository Naming Convention


## Purpose

This guide standardizes the naming of GitHub repositories within our organization to increase clarity, searchability, and consistency. Adherence to this guide ensures that our repositories are easy to locate and understand, facilitating collaboration and communication.

:::caution
Not adhering to these naming conventions will result in an audit failure.
:::

## Naming GitHub Repositories

[//]: # (Our naming convention comprises three key components separated by hyphens: `{technology}-{project}-{module}`.)

All repositories should follow the following naming convention:

`{technology}-{project}-{module}`
- `{technology}` - The primary technology or programming language used in the repository. This could include `python`, `java`, `react`, `nodejs`, etc. This tag aids developers in identifying the principal technology stack used in the project.
- `{project}` - The name of the broader project or initiative that the repository belongs to. This could include `payment-system`, `user-authentication`, `data-analytics`, etc. This tag helps categorize repositories by their overarching project or function.
- `{module}` - This tag refers to the specific function of the code in the repository. This could be `frontend`, `backend`, `api`, `database`, etc. In the case of repositories that contain a microservice or a library, this tag could represent its specific purpose.

:::tip EXAMPLES
By combining these components, repository names like `react-ecommerce-frontend`, `java-payment-system-api`, and `python-data-analytics-processing` can be formed.
:::
:::caution
It must be enfatized that all characters in the repository name must be lowercase and separated by hyphens (kebab-case). This is to ensure that the repository name is compatible with all systems.
See more information on [kebab-case](#why-use-kebab-case-in-repository-naming).
:::

### Additional Guidelines

- **Clarity:** Ensure that the repository names are understandable even to newcomers. Avoid using acronyms or jargon unless they are widely recognized.

- **Consistency:** Apply these rules consistently across all repositories. Consistency reduces confusion and aids in quickly identifying the purpose of a repository.

- **Simplicity:** The naming convention should be simple but informative. Avoid including unnecessary information, but also don't omit information that aids in identifying the repository's purpose.

- **Searchability:** Use terms that are likely to be included in search queries to increase the visibility of the repository.

- **Uniqueness:** Each repository name within the organization should be unique to avoid confusion and facilitate specific repository searches.

- **Avoid Special Characters:** Stick to lowercase letters, numbers, and hyphens to prevent potential issues with certain systems.

<br></br>

### Kebab Case

These are the reasons why we use kebab-case in our repository naming convention:

- **URL Friendliness:** The most significant advantage of kebab-case is its compatibility with URLs. Browsers interpret spaces in URLs as `%20`, which makes the URL hard to read. Kebab-case, with its hyphen-separated syntax, makes URLs more readable and user-friendly.
- **Universally Recognized:** Kebab-case does not rely on capitalization to separate words, making it easy to read across various cultures and languages. Unlike camelCase, which could be difficult to interpret for individuals unfamiliar with the convention, kebab-case is straightforward and intuitive.
- **System Compatibility:** Some systems interpret capital letters in camelCase as commands or different characters, which can lead to errors. Kebab-case avoids this issue by using only lowercase letters.
- **Visual Clarity:** Kebab-case improves readability by visually separating words with hyphens. This makes long and complex repository names easier to understand at a glance.


### Examples

In this section, we will illustrate the application of our `{technology}-{project}-{module}` naming convention using a variety of examples. Each example has been chosen to represent a common scenario that you might encounter when creating a new repository.

1. **React-based Ecommerce Project:**
    - Frontend Repository: `react-ecommerce-frontend`
    - Backend Repository: `nodejs-ecommerce-backend`
    - API Repository: `express-ecommerce-api`

2. **Java-based Payment System:**
    - API Repository: `java-payment-system-api`
    - Database Repository: `sql-payment-system-db`
    - Fraud Detection Microservice: `java-payment-system-fraud-detection`

3. **Python-based Data Analytics Project:**
    - Data Processing Repository: `python-data-analytics-processing`
    - Visualization Repository: `d3-data-analytics-visualization`
    - Machine Learning Repository: `python-data-analytics-ml`

4. **Angular-based User Authentication Project:**
    - Frontend Repository: `angular-user-authentication-frontend`
    - Backend Repository: `nodejs-user-authentication-backend`
    - API Repository: `express-user-authentication-api`

5. **Django-based Blogging Platform:**
    - Frontend Repository: `html-django-blog-frontend`
    - Backend Repository: `python-django-blog-backend`
    - Database Repository: `sql-django-blog-db`

:::tip
If you are unsure about how to name a repository, you can always ask for help from your team members or the organization's leadership.
Also try and search for similar repositories in the organization or over GitHub to see how they are named.
:::

# Exceptions and Edge Cases

Sometimes, a repository might not fit neatly into the `{technology}-{project}-{module}` format. Here are a few examples of how to handle these situations:

1. **Multi-Technology Repositories:** If a repository uses multiple technologies, you can use the one that is most representative or the one used the most. For instance, if you have a Full Stack application using both React and Node.js, you might name it `react-node-fullstack-app`.

2. **Common Libraries or Utilities:** If a repository is a common library or utility used across several projects, it might not have a specific project name. In this case, you could use `lib` or `util` as the project name. For instance: `java-lib-logging` or `python-util-data-cleaning`.

3. **Documentation Repositories:** If a repository is used for documentation, you could use `doc` as the technology. For instance: `doc-ecommerce-api` for the API documentation of the Ecommerce project.

Remember, the goal of these guidelines is to create clear, descriptive repository names. If a name doesn't seem clear, consider whether there's a better way to structure it.

## Conclusion

Adherence to this guide will ensure a high level of organization and clarity across all GitHub repositories within our organization. This will help facilitate collaboration and communication among team members, ultimately contributing to more effective and efficient development processes.

