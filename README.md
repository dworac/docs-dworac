# @dworac/docs

This is the repository for `@dworac/docs`, a project that uses Docusaurus v2.4.1 to generate a static website with documentation.

View the documentation at [https://dworac.github.io/docs/](https://docs.dworac.com).

## Prerequisites

Ensure that you have Node.js v16.14 (or later) installed on your machine before proceeding and yarn installed globally.

## Installation

To install all necessary dependencies, navigate to the repository's root directory in your terminal and run:

```bash
yarn
```

## Available Scripts

In the project directory, you can run:

```bash
yarn start
```

Runs the website in the development mode. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

```bash
yarn build
```

Builds the website for production to the `build` folder. It correctly bundles React in production mode and optimizes the build for the best performance.

```bash
yarn swizzle
```

Copies the theme files into your website. Be careful as this command will override any existing files with the same name.

```bash
yarn deploy
```

Builds and deploys the website. This command is a shorthand for running `docusaurus build` and `docusaurus deploy`.

```bash
yarn clear
```

Deletes the cache and generated files.

```bash
yarn serve
```

Serves the content of the `build` directory as a static site. Useful for testing the build output.

```bash
yarn write-translations
```

Dumps the default messages that would be translated.

```bash
yarn write-heading-ids
```

Overwrites Markdown files in-place with heading IDs using the GitHub algorithm.

## Contributing
If you have any suggestions or improvements, please feel free to create a pull request or submit an issue.

## License
This project is licensed under the MIT license. Please see the LICENSE file for more information.
