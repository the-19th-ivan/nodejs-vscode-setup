# Node.js - VS Code Setup

This documentation provides a detailed guide on setting up Visual Studio Code (VS Code) for Node.js development. The following steps will walk you through the installation process and the configuration of ESLint, Prettier, and the Airbnb Style Guide.

## Installation

To set up your development environment, follow these steps:

1. **Install VS Code**: Download and install the latest version of [Visual Studio Code](https://code.visualstudio.com/).

2. **Install ESLint and Prettier Extensions**: Open VS Code, navigate to the Extensions view, and search for "ESLint" and "Prettier" extensions. Install the ones published by the respective authors.

3. **Set up your Node.js application**: Open your terminal or command prompt, navigate to your project directory, and initialize a new Node.js application by running the following command:

```bash
npm init
```

4. **Install ESLint and Prettier Packages**: In the terminal, install the necessary npm packages for ESLint and Prettier by running the following command:

```bash
npm i -D eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-node eslint-plugin-prettier eslint-plugin-react prettier
```

## Configuration

Once you have completed the installation, you need to configure ESLint and Prettier for your project.

1. **Create the .prettierrc File**: In your project's root directory, create a file named **`.prettierrc`** and copy the following configuration into it:

```bash
{
  "singleQuote": true
}
```

This configuration enables the use of single quotes for strings in your code.

2. **Create the .eslintrc.json File**: In your project's root directory, create a file named **`.eslintrc.json`** and copy the following configuration into it:

```bash
{
  "extends": ["airbnb", "prettier", "plugin:node/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "spaced-comment": "off",
    "no-console": "warn",
    "consistent-return": "off",
    "func-names": "off",
    "object-shorthand": "off",
    "no-process-exit": "off",
    "no-param-reassign": "off",
    "no-return-await": "off",
    "no-underscore-dangle": "off",
    "class-methods-use-this": "off",
    "prefer-destructuring": ["error", { "object": true, "array": false }],
    "no-unused-vars": ["error", { "argsIgnorePattern": "req|res|next|val" }]
  }
}
```

This configuration extends the Airbnb style guide, integrates Prettier, and includes recommended rules for Node.js development. Additionally, it disables or adjusts certain rules to match common preferences and practices.

## Usage

With the setup and configuration complete, you can now start developing your Node.js application using VS Code. ESLint will provide real-time linting and static analysis, while Prettier will format your code automatically according to the specified rules.

You can customize the ESLint rules or add more plugins according to your project's requirements. For advanced configuration options, refer to the respective documentation for ESLint, Prettier, and the Airbnb style guide.

Happy coding!
