# Changelog Generator 

This repo is used as an example repository to show how changelogs can be generated automatically. 

## Prerequisites 
* Conventional Commits are a prerequisite to generate changelogs. 
* Squash commits for every branch that goes into main line? -> probably not needed, but commits that belong together to a feature for example should be squashed. 
* PR merge with no merge commit (fast forward)

## Conventional Commits
* Originates from the Angular project
* Commit Message structure
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]

* Commit types
  * feat: a commit of the type fix patches a bug in your codebase (this correlates with PATCH in Semantic Versioning)
  * fix: a commit of the type feat introduces a new feature to the codebase (this correlates with MINOR in Semantic Versioning).
  * chore
  * docs 
  * style
  * refactor
  * perf
  * test

* BREAKING CHANGE: a commit that has a footer BREAKING CHANGE:, or appends a ! after the type/scope, introduces a breaking API change (correlating with MAJOR in Semantic Versioning). A BREAKING CHANGE can be part of commits of any type
* Be careful when resolving conflicts, to still keep the conventional commit message. Maybe ammeding could work here. 

## Tooling 
* https://github.com/commitizen/cz-cli, downside: needs a nodejs project
* https://marketplace.visualstudio.com/items?itemName=vivaxy.vscode-conventional-commits
* https://github.com/cocogitto/cocogitto

## Working with cocogitto 
* Ignoring merge commits is possible via cofig

## Additional Information
* https://www.conventionalcommits.org/en/v1.0.0/ 
