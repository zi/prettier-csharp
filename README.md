<p align="center">
    :construction: Work in Progress! :construction:
</p>

<div align="center">
<img alt="Prettier"
  src="https://cdn.rawgit.com/prettier/prettier-logo/master/images/prettier-icon-light.svg">
<img alt="C#"
  hspace="25"
  height="210"
  src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Csharp_Logo.png">
</div>

<h2 align="center">Prettier C# Plugin</h2>

<p align="center">
  <a href="https://gitter.im/jlongster/prettier">
    <img alt="Gitter" src="https://img.shields.io/gitter/room/jlongster/prettier.svg?style=flat-square">
  </a>
  <a href="https://travis-ci.org/warrenseine/prettier-csharp">
    <img alt="Travis" src="https://img.shields.io/travis/warrenseine/prettier-csharp/master.svg?style=flat-square">
  </a>
  <a href="https://www.npmjs.com/package/prettier-csharp">
    <img alt="npm version" src="https://img.shields.io/npm/v/prettier-csharp.svg?style=flat-square">
  </a>
  <a href="#badge">
    <img alt="code style: prettier" src="https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square">
  </a>
  <a href="https://twitter.com/PrettierCode">
    <img alt="Follow+Prettier+on+Twitter" src="https://img.shields.io/twitter/follow/prettiercode.svg?label=follow+prettier&style=flat-square">
  </a>
</p>

## WORK IN PROGRESS

Please note that this plugin is under active development, and might not be ready to run on production code yet. **It will break your code.**

## Install

```bash
yarn add --dev --exact prettier prettier-csharp
```

## Use

```bash
prettier --write "**/*.cs"
```

## How it works

The plugin is written in JavaScript. It depends on the JavaScript port of ANTLR and an
[unmodified unofficial C# 6 grammar from ANTLR](https://github.com/antlr/grammars-v4/tree/master/csharp).
The grammar is precompiled to plain JavaScript and ready to use in the project.

## Contributing

### Updating the grammar

- Copy the latest version of the [grammar](https://github.com/antlr/grammars-v4/tree/master/csharp) to `asset/csharp`
- Install ANTLR:

```bash
brew install antlr4 # on macOS
```

- Generate the JavaScript parser:

```bash
yarn install
yarn generate-parser
```

### Testing

The project is developed against a single grammar-complete regression test. There are no unit tests for the moment.

Run the test with:

```bash
yarn test
```

To test it out on an actual C# file:

- Clone this repository.
- Run `yarn`.
- Create a file called `test.cs`.
- Run `yarn prettier test.cs` to check the output.

## Maintainers

<table>
  <tbody>
    <tr>
      <td align="center">
        <a href="https://github.com/warrenseine">
          <img width="150" height="150" src="https://github.com/warrenseine.png?v=3&s=150">
          </br>
          Warren Seine
        </a>
      </td>
    </tr>
  <tbody>
</table>
