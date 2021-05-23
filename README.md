# Vite Sandbox Shell Script

A simple script to streamline creating a [Vite](https://vitejs.dev/) sandbox. It defaults to a React template and performs a few related cleanup operations. You likely want to use this as a basis for adding your own customizations instead.

This script requires [Yarn](https://yarnpkg.com/). Simply replace all mentions of `yarn` to use NPM instead.

## Features

- Add a default template (React) and default folder name
- Execute a few cleanup operations for the React template
- Automatically open the sandbox as a workspace in VS Code

## Installation

Download the [latest release](https://github.com/kgrhartlage/vite-sandbox-script/releases/download/v0.0.1/vite-sandbox) and move the script file to a directory included in your `PATH` environment variable. Conventional paths for user scripts are `/usr/local/bin` or `/opt/bin`. Then make the script executable:

```bash
 $ chmod +x vite-sandbox
```

## Usage

Execute the script using the `vite-sandbox` command. The sandbox will always be created at `$HOME/Desktop`, regardless of your current working directory.

### Options

#### Folder Name

If no additional argument is provided to the `vite-sandbox` command, the current date will be attached to the folder name:

```bash
$ vite-sandbox
# => sandbox-YYYY-MM-DD
```

The date can be replaced by providing an argument to the `vite-sandbox` command:

```bash
$ vite-sandbox custom-name
# => sandbox-custom-name
```

#### Template

The script defaults to a React template. You can override this by providing a second argument that specifies a supported [template name](https://vitejs.dev/guide/#scaffolding-your-first-vite-project):

```bash
$ vite-sandbox custom-name vue-ts
# creates a Vue TypeScript project
```

## License

Released under the terms of the [MIT License](https://opensource.org/licenses/MIT).
