# Project Environment

## Introduction

In here we'll discuss about the project environment. We'll discuss about the project architecture & folder structure, project environments (`Production`, `Development`, `Staging`), how secrets `(environment variables)` are handled, how to use environment variables for different environments,

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
└── yarn.lock
```

### Project Environments

The project has three environments. They are `Production`, `Development`, `Staging`. For each type of environment, we have a separate `.env` file. [Read more about environment variables](#environment-variables--how-we-use-them).

### Environment Variables & How we use them

The environment variables for the project are stored in three `.env` files and we have a common `.env` file to store the common environment variables. The `.env` files are stored in the root directory of the project. The `.env` files are as follows.

-   `.env` - This file contains the common environment variables for all the environments.
-   `.env.development` - This file contains the environment variables for the `Development` environment.
-   `.env.staging` - This file contains the environment variables for the `Staging` environment.
-   `.env.production` - This file contains the environment variables for the `Production` environment.

The environment variables will be loaded based on the environment. For example, if the environment is `Development`, then the environment variables from `.env` and `.env.development` will be loaded. If the environment is `Staging`, then the environment variables from `.env`, `.env.development` and `.env.staging` will be loaded. If the environment is `Production`, then the environment variables from `.env`, `.env.development`, `.env.staging` and `.env.production` will be loaded. The environment will be determined based on the `NODE_ENV` environment variable in `.env` file. If the `NODE_ENV` environment variable is not set, then the environment will be set to `Development`.
