# Contributing

The project is divided into multiple micro-services, each represented by a repository. **All repository** **follow the workflow below**.

Please be aware of the 2 main keywords when reading this document:

- **must** : indicates that it is a **required** rule to follow
- **should** : indicates that it is a **recommended** rule to follow

## Gitflow

---

1. Create an Issue
2. Create a feature branch related to the Issue
3. Develop, you can optionally open a draft PR
4. Undraft or create a PR to merge it on main
5. Resolve conflict & rebase before merging

There is 2 type of branch :

- The main branch, stable, it is the actual state of the app in staging
- Feature branches, for development, one or more branch per Issue

Each time you want to develop something new you **must** create an Issue and a feature branch linked to It. The branch will be merged on main **only with a PR**. This workflow is based on the [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow).

## Issues

---

### When to make an Issue

An Issue should be opened each time you want to develop on a repository, it could be for a **feature request**, **bug fix** or a new **documentation** entry. You **must** open an Issue before creating any feature branch. An Issue is a formal and understandable way to describe a problem/an idea, it shouldn't be technical.

### How to make an Issue

There is 2 templates for Issues, you’ll have to chose the best that fits with your needs and you **must** follow it in order to make your Issue more readable.

The **title** of your Issue should be concise and represent the topic you’re working on, for example : `Working on contribution`.

The **body** of an Issue follow a series of question to introduce the problem, followed by a **task list** that will describe every steps in order to tag the Issue as resolved.

After creating your Issue you’ll need to create one or more feature branch and link them to the Issue, to link a branch to the Issue you can use the `Development` section located in the right panel when in the Issue’s page on GitHub.

## Commits

---

Your commits should follow the [conventional commits specification](https://www.conventionalcommits.org/en/v1.0.0/#summary).

You should follow these basic rules :

- A commit message has a title ( summary ), body and footer
- The title should be 50 characters maximum
- Put a blank line between the title, body and footer
- Describe what and why, but not how ( the purpose, not the implementation )
- The footer describe any additional data such as breaking changes

## Pull Requests

---

### When to make a Pull Request

You should open a PR as soon as you’ve created you’re feature branch, though you can mark it as draft or put the tag `WIP`. You **must** create a PR if you want to merge your work into the main branch.

### How to make a Pull Request

You **must** follow the template provided in order to make your PR more readable.

The **title** of your PR should be concise and represent the topic you’ve worked on, for example : `Contribution Template`.

The **body** of a PR follow a series of question to introduce the solution, followed by a **task list** that will describe every steps in order to tag the PR as reviewable, the task list **must** be the same as the related Issue but it should be more technical and describe in details the decisions you’ve taken.

There are 2 **required** types of labels that you **must** put on your PR :

- Version label (`version/major`, `version/minor`, `version/patch`) : these are label indicating how heavy is your update, you **must** follow the [semantic versioning convention](https://semver.org) when making a PR.
- Topic label (`enhancement`, `bug fix`, `documentation`) : these are label indicating what type of PR you want to merge. They will be handled by the release drafter to generate a change log.

### How to review a Pull Request

A PR **must** have at least 1 approve in order to be merged, if you’ve found something to say open a discussion on the PR page.

After turning your PR as reviewable every modification should appear as a `fixup` commit so every one can follow the resolution history. To tag a commit as fixup just add the flag `--fixup` when committing.

When all discussion are resolved and the PR is ready to merge, you can rebase with the `--autosquash` flag to squash the `fixup` commits and let only the main ones. For more information on this workflow please follow [this article on fixup commits](https://www.mikulskibartosz.name/git-fixup-explained/)
