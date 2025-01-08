# Welcome!

## Don't know where to start?

- report an *issue* or suggest new *content* -- open an [issue] on *GitHub*
- improve the *documentation* -- suggest changes in the various READMEs if instructions are unclear

[issue]: https://github.com/BecksLab/website/issues

## Setting up your environment

Have a look at the current [Julia documentation][pkgdoc].

[pkgdoc]: https://docs.julialang.org/en/stable/manual/packages/#Making-changes-to-an-existing-package-1

## EMOJIS!

Please use emojis, this helps visually sorting through the commits (and makes for a 
fun time). Inspiration taken from [sciencegitmojis](https://github.com/MichielStock/sciencegitmojis)

| If the commit is about...                               | ...then use                | Example                                        |
|:--------------------------------------------------------|:---------------------------|:-----------------------------------------------|
| Work in progress                                        | `:construction:`           | :construction: new output structure            |
| Bug fix                                                 | `:bug:`                    | :bug: mean fails if NA                         |
| Fixing typos                                            | `:pencil2:`                | :pencil2: README                               |
| Code maintenance                                        | `:wrench:`                 | :wrench: fix variable names                    |
| New test                                                | `:clapper:`                | :clapper: wget JSON resource                   |
| Plot figures                                            | `:bar_chart:`              | :bar_chart: example boundaries                 |
| New data                                                | `:cd:`                     | :cd: example pollination network               |
| New feature                                             | `:sparkles:`               | :sparkles: (insert achievement)                |
| Documentation                                           | `:books:`                  | :books: lattice function                       |
| Performance improvement                                 | `:racehorse:`              | :racehorse: parallelizes models by default     |
| Upcoming release                                        | `:package:`                | :package: v1.0.6                               |
| Ugly but working code                                   | `:dragon:`                 | :dragon: added lattice function                |
| Working on code that doesn't work but I want to go home | `:neutral_face:`           | :neutral_face: for triangulation               |
| I forgot to save everything before committing           | `:sandwich:`               | :sandwich: what is saving                      |
| Jettisoned something                                    | `:boom:`                   | :boom: manifest                                |

## Workflow 

This section describes the general steps to make sure that your contribution is
integrated rapidly. Note that the `main` branch is protected and you will be 
unable to make any changes directly but rather through pull requests. The 
general workflow is as follows:

1. Create an [issue] that outlines proposed *content* or *fixes*
2. Fork the repository (see *Branches, etc.* below)
3. Create an *explicitly named branch* from `main`
4. Create a pull request *as soon as you make the first commit* and link this to the relevant issue
5. Be as explicit as possible on your goals
6. Do not squash / rebase commits while you work -- we will do so when merging

### Pull requests

Creating a pull request *before* you push any code will signal that you are
interested in contributing to the project. Once this is done, push often, and be
explicit about what the commits do (see commits, below). This gives the
opportunity for feedback during your work, and allow for tweaks in what you are
doing.

A *good* pull request (in addition to satisfying to all of the criteria below)
is:

1. Single purpose - it should do one thing, and one thing only
2. Short - it should ideally involve less than 250 lines of code
3. Limited in scope - it should ideally not span more than a handful of files
4. Well tested and well documented
5. Written in a style similar to the rest of the codebase

This will ensure that your contribution is rapidly reviewed and evaluated.

### Deployment

While you are working on changes you can render the site locally using 
`quarto render` and if you want to preview it you can use `quarto preview`.

The website itself is deployed through github actions and is the reason that we 
will use pull requests as a way to not only act as a checkpoint as to what 
content is added to the website but also as a means to test that any changes that
are made to the files will not break the deployment workflow.

This is all automated and you *should* not need to manually activate these deployments 
however, if they fail you will not be able to merge your pull request and it is
at this point that you will need to work out what has caused the build to fail.
You can refer to the build logs on Github but it might be easier to run 
`quarto render` locally and see what the error messages are from there.

The only time that you will need to first render the site locally before publishing
is if you modify any code-based content. This is because we use the freeze 
functionality that allows us to store partial builds of the website nad makes remote 
rendering mush more efficient. Currently this will only apply to changes made to the
collaborators map in `people.yml`.