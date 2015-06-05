# cut-release

A command line tool that helps you make faster npm releases.

![](https://raw.githubusercontent.com/bjoerge/cut-release/master/demo.gif)

# What it does:

  * runs `npm version` with the version you specify. If run in a git repo, it will also create a version commit and tag, just like what [`npm version`](https://docs.npmjs.com/cli/version) does.
  * pushes commits and tags to origin
  * runs `npm publish`

# Install

    npm install -g cut-release

# Usage 

```
Usage: cut-release [<newversion> | patch | minor | major | prepatch | preminor | premajor | prerelease]


  Options:

    --yes, -y       Don't confirm, just release right away. The new version must be supplied.

```
