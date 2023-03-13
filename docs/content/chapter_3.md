# Project Environment

## Introduction

Here we'll discuss about,

-   Project environment
-   Project architecture & Folder structure
-   Project environments (`Production`, `Development`, `Staging`),
-   How secrets `(environment variables)` are handled
-   How to use environment variables for different environments,

### Project Architecture & Folder Structure

The project architecture is based on the [Next.js](https://nextjs.org/) framework. The project folder structure is as follows.

```bash
├── .github
│   └── workflows
│       └── ci.yml
├── .next
│   ├── cache
│   ├── dist
│   ├── server
│   └── static
├── .vscode
│   └── settings.json
├── components
│   ├── common
│   │   ├── Button
│   │   │   ├── index.js
│   │   │   └── styles.js
│   │   ├── Card
│   │   │   ├── index.js
│   │   │   └── styles.js
│   │   ├── Footer
│   │   │   ├── index.js
│   │   │   └── styles.js
│   │   ├── Header
│   │   │   ├── index.js
│   │   │   └── styles.js
│   │   ├── Layout
│   │   │   ├── index.js
│   │   │   └── styles.js
│   │   └── Navbar
│   │       ├── index.js
│   │       └── styles.js
│   └── pages
│       ├── blog
│       │   ├── [slug].js
│       │   └── index.js
│       ├── index.js
│       └── post
│           └── [...all].js
├── next.config.js
├── package.json
├── pages
│   ├── _app.js
│   ├── _document.js
│   ├── _error.js
│   ├── blog
│   │   ├── [slug].js
│   │   └── index.js
│   ├── index.js
│   └── post
│       └── [...all].js
├── public
│   ├── favicon.ico
│   └── images
│       └── logo.png
├── README.md
├── styles
│   ├── global.js
│   └── theme.js
```

### Project Environments

The project has three environments.

-   `Production` → _(Host the live version of the project and deploy the final release to the public)_
-   `Development` → _(Develop and test new features and changes before they are released to Staging and Production)_
-   `Staging` → _(Test the project with real data)_

For each type of environment, we have a separate .env file because it allows us to control what environment the project is running in and provide any environment-specific variables such as passwords, credentials, or API keys.

We use different databases for each environment since it helps to guarantee that production data is used only in production and staging data is used only in staging.

We also use different servers for each environment, so the production server is separate from the staging server. It helps to protect that production code is only deployed to production and staging code is only deployed to staging.

### Environment Variables & How we use them

The environment variables for the project are stored in three `.env` files and we have a common `.env` file to store the common environment variables. The `.env` files are stored in the root directory of the project. The `.env` files are as follows.

-   `.env` - Contains the common environment variables for _all three_ environments.
-   `.env.development` - Contains the environment variables for the `Development` environment.
-   `.env.staging` - Contains the environment variables for the `Staging` environment.
-   `.env.production` - Contains the environment variables for the `Production` environment.

<br/>
The environment variables will be loaded based on the environment. For example,

-   If the environment is `Development`, then the environment variables from `.env` and `.env.development` will be loaded.
-   If the environment is `Staging`, then the environment variables from `.env`, `.env.development` and `.env.staging` will be loaded.
-   If the environment is `Production`, then the environment variables from `.env`, `.env.development`, `.env.staging` and `.env.production` will be loaded.

| Environment | Effective File Name           |
| :---------- | :---------------------------- |
| Development | `.env` and `.env.development` |
| Staging     | `.env` and `.env.staging`     |
| Production  | `.env` and `.env.production`  |

The environment will be determined based on the `NODE_ENV` environment variable in `.env` file. If the `NODE_ENV` environment variable is not set, then the environment will be set to `Development`.
