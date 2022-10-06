# Changelog Generator 

This repo is used as an example repository to show how changelogs can be generated automatically. 

## Prerequisites 
* Conventional Commits are a prerequisite to generate changelogs. 
* Commits that belong together to a feature for example should be squashed. 
* PR merge with no merge commit (fast forward)

## Conventional Commits
* Originates from the Angular project
* Commit Message structure
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]

* Commit types
  * fix: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning)
  * feat: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
  * chore
  * docs 
  * style
  * refactor
  * perf
  * test

* BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type
* Be careful when resolving conflicts, to still keep the conventional commit message. Maybe ammeding could work here. 

## Working with cocogitto 
* Note that cocogitto can be used for both, helping with conventional commits and with generating change logs as well as versioning. For helping with conventional commits you could also use some other tool like for example the visual studio plugin. We will focus on the changelog generating and versioning and therefore stick to use cocogitto. 
* Install Rust on your machine: https://www.rust-lang.org/tools/install 
* Install cocogitto CLI: https://docs.cocogitto.io/#installation
* 
* commit using `cog commit <type> "<message>"`. For breaking changes, append `-B`
* Show changelog using `cog changelog`
* Bump version using `cog bump --auto` or `cog bump --version 1.2.0`

Notes:
* Note that ignoring merge commits is possible via config
* Prefixes for tags can be configured
* Auto bumping uses commit messages to determine the next version number. 
  * Unless version is below 1.0.0, auto bumping will increase major version if there was any breaking change commit.
  * If there was no breaking change commit, only features only minor version is increased. 


## Additional Information
* https://www.conventionalcommits.org/en/v1.0.0/
* https://github.com/cocogitto/cocogitto

## Other Tooling
* https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits
* https://github.com/commitizen/cz-cli, downside: needs a nodejs project 
