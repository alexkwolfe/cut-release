# cut-release

A command line tool that helps you make faster npm releases.

![](https://raw.githubusercontent.com/activeprospect/cut-release/master/demo.gif)

# What it does:

  * If run in a git repo, ensures that the local repo has no uncommitted changes, that the tracked remote repo
    are in sync and that the git tag doesn't already exist
  * runs `npm version` with the version you specify. If run in a git repo, it will also create a version commit and tag,
    just like what [`npm version`](https://docs.npmjs.com/cli/version) does.
  * pushes commits and tags to the remote repo
  * runs `npm publish` and tags the published module

# Install

    npm install -g cut-release

# Usage 

```
Usage: cut-release [<newversion> | patch | minor | major | prepatch | preminor | premajor | prerelease]


  Options:

    --yes, -y       Don't confirm, just release right away. The new version must be supplied.

    --message, -m   If supplied, npm will use it as a commit message when
                    creating a version commit. If the message contains %s then
                    that will be replaced with the resulting version number

    --tag, -t       The NPM tag to use when publishing. Defaults to 'latest'. Use this option with
                    no value to choose from a list of existing tags.

    --preid, -p     The NPM prerelease identifier to be used when a prerelease version is specified.

    --dry-run, -d   Print the commands to be executed without actually running them.
```
