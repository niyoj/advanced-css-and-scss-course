# NPM Guides
## Initializing a Project (NPM INIT)
- `npm init` command is used to initialize npm project and creates file `package.json`.
- `package.json` stores all the metadata like name, version, description, dependencies and develope dependencies and their versions etc.
- `npm init --yes` shorthanf command to initialize a project ASAP.

## Installing Moudles (NPM INSTALL <MODULE>)
- `npm install <module>` is used to install a module in the project where, `<module>` is its name.
- The module are always installed inside `./node_modules` folder and saves them to the `package.json` as a dependency.
- The shorthand command for installation is `npm i <module>`.

### Installing as a Developer Dependencies
- The key difference between developer dependencies and dependencies is that dependencies are for the production level and developer dependecies is for development only.
- The shorthand command is `npm install <module> --save-dev` for installation of devDependencies.

### Installing Globally on system
- `npm install <module> -g` OR `npm install <module> --global` is used to perform this action.

## NPM Scripts (NPM RUN <STAGE>)

### LifeCycle Scripts
```json
{
  "scripts": {
    "precompress": "{{ executes BEFORE the `compress` script }}",
    "compress": "{{ run command to compress files }}",
    "postcompress": "{{ executes AFTER `compress` script }}"
  }
}
```