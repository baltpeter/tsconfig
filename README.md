# @baltpeter/tsconfig

> The TypeScript configs I use for my projects.

This package contains the TypeScript configs I use for my projects. You probably don't want to use this unless you're working on a project with me.

## Usage

Install TypeScript and this config:

```sh
yarn add --dev typescript @baltpeter/tsconfig
```

Then, create a `tsconfig.json` file like this:

```json
{
    "extends": "@baltpeter/tsconfig",
    "include": ["src/**/*"]
}
```

Make sure to adapt the `include` property if necessary.

Instead of the default config, you can also use one of the following configs:

* `@baltpeter/tsconfig/tsconfig.node.json` for Node.js projects
* `@baltpeter/tsconfig/tsconfig.preact.json` for Preact projects

   For the aliasing of React to Preact to work, you need to set `"baseUrl": "./"` in _your_ `tsconfig.json`, e.g.:

   ```json
   {
        "extends": "@baltpeter/tsconfig/tsconfig.preact.json",
        "include": ["src/**/*"],

        "compilerOptions": {
            "baseUrl": "./"
        }
    }
   ```
