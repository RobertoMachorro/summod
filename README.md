# summod

A numbers addition module. The intent is to demonstrate how _node modules_ work, and make the module available via _GitHub Packages_.

## Installing

NPM wants to always pull from it's home repository. You have to indicate that you are fetching from a different repository based on scope, use an *.npmrc* file:

```
@robertomachorro:registry=https://npm.pkg.github.com/
registry=https://registry.npmjs.org/
```

Or login to GitHub Package (use an Access Token), then install the module:

```
npm login --registry=https://npm.pkg.github.com/ --scope=@robertomachorro
npm install @robertomachorro/summod
```

## Installing for Debug

NPM allows local installations, these don't require the module to be pulled down from a repository.

```
npm help link
npm link
npm link @robertomachorro/summod
```

## Usage

Within code:

```
const summod = require('@robertomachorro/summod')
const summodarr = require('@robertomachorro/summod/sumarray')

console.log('Demo', summod.sum(1, 2), summodarr.addall(0))
```

## References

* [Creating NodeJS modules](https://docs.npmjs.com/creating-node-js-modules)
* [Configuring NPM for use with GitHub Packages](https://help.github.com/en/packages/using-github-packages-with-your-projects-ecosystem/configuring-npm-for-use-with-github-packages)
