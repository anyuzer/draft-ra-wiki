# Publishing NPM Packages

## Why
We need to be able to share code in different applications and version the shared code. Distributing these them as NPM packages is the approach we agreed on.

## What
A package is just a directory with one or more files in it, that also has a file called "package.json" with some metadata about this package. A typical application, such as a website, will depend on dozens or hundreds of packages. These packages are often small. The general idea is that you create a small building block which solves one problem and solves it well. This makes it possible for you to compose larger, custom solutions out of these small, shared building blocks.

## How
1. Create the directory with package.json and run `npm shrinkwrap` after installing packages
2. If you are transpiling code, transpile into a lib folder.
3. add .gitignore to ignore the lib folder
4. add empty .npmignore so that lib can be part of the package distribution.
5. commit and push to github
6. publish the package with following commands:
  - `npm version (major | minor | patch)`
  - `git push && git push --tags`
  - `npm publish`


### Recommended file structure
```bash
myPackage/
|-- src/
|-- lib/
|-- .eslintrc
|-- .gitignore
|-- .npmignore
|-- .babelrc
|-- package.json
|-- npm-shrinkwrap.json
|-- README.md
```
