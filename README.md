# cut-release

A command line tool that helps you make faster NPM releases.

# What it does:

  * If run in a git repo, ensures that the local repo has no uncommitted changes, that the local branch is tracking
    a remote branch, that the remote branch is not ahead of the local branch, and that the git tag doesn't already
    exist
  * runs `npm version` with the version you specify. If run in a git repo, it will also create a version commit and tag,
    just like what [`npm version`](https://docs.npmjs.com/cli/version) does.
  * pushes commits and tags to the remote repo
  * runs `npm publish` and tags the published module

# Install

    npm install -g @activeprospect/cut-release

# Usage 

To see usage documentation, run `cut-release --help`:

```
$ cut-release --help

Usage: cut-release [increment] [options]

Supported increments: <semver>, patch, minor, major, prepatch, preminor, premajor, prerelease

Options:
  -y, --yes       Skip confirmation when present  [boolean] [required] [default: false]
  -t, --tag       NPM tag for the release (i.e. latest, next)  [string]
  -p, --preid     NPM prerelease identifier (i.e. rc, alpha, beta)  [string]
  -d, --dry-run   Print commands to be run, but don't run them  [boolean] [default: false]
  -m, --messasge  Version commit message - the %s variable will be replaced with the version  [string]
  -h, --help      Show help  [boolean]
  -v, --version   Show version number  [boolean]
```
