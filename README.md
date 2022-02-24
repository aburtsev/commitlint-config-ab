# commitlint-config-ab

This is the configuration for the (commitlint)[https://github.com/conventional-changelog/commitlint]

Inspired by (Angular Commit Message Guildlines)[https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines], but with some flavors.

Basic specification is (Conventional Commits)[https://www.conventionalcommits.org/en/v1.0.0/]

## Getting started

### Install 

```
npm install --save-dev @commitlint/{config-conventional,cli} commitlint-config-ab
```

### Setup
```
echo "module.exports = {extends: ['@commitlint/config-conventional', 'ab']}" > commitlint.config.js
```

### husky integration
```
# Install Husky v6
npm install husky --save-dev
# or
yarn add husky --dev

# Activate hooks
npx husky install
# or
yarn husky install

# Add hook
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'
```

If it doesn't work check the (Getting Started for commitlint)[https://github.com/conventional-changelog/commitlint#getting-started]

## Format
```
type(scope?): subject  // header

[optional body] // body

[optional footer(s)] // footer
```


## rules

### basics

- Max header lenght is 50 chars (as linux standard)

### types

**fix:** a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning).
**feat:** a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
**revert:** revert commits or downgrading dependencies
**bump:** dependencies updates
**dev:** Changes that affect the build system or changes to our CI configuration files and scripts
**refactor:** A code change that neither fixes a bug nor adds a feature
**docs:** Documentation only changes
**perf:** A code change that improves performance
**test:** Adding missing tests or correcting existing tests
**style:** Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)


