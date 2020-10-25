# Contributing

## Install Rush and Pnpm

Before anything you need two tools: `pnpm` and `@microsoft/rush`
You can install them with the `npm install -g` like this:

``` shell
npm install -g pnpm
npm install -g @microsoft/rush
```

## Start writing code

Before you can start making changes it's mandatory to run this command:

` `  ` pnpm install && rush update `  ` `
for installing all the dependencies.

After that you can start coding, the source folders are `core` , `components` , `presets` and `shapes` .

The `core` folder contains tsParticles library, the main library.

The `components` folder contains all javascript frameworks wrappers built around tsParticles: Angular, jQuery, Preact, React, Vue.

The `presets` and `shapes` folder contains all external presets and shapes.

Once done editing you can check if everything builds running `rush build` .

The difference is the first does not create the docs folder and it can be unnecessary while coding.

## Testing

There's a small demo app inside the repository in the `core` folder, just run `yarn start` and go to http://localhost:3000

The `presets` and `shapes` doesn't have a demo app inside the repository for now.

A demo folder will be probably created in near future with all the demo apps needed.

---

# Pull Requests

**Before opening any pull request check that `rush build` completes**

*The build task will be performed automatically by the CI\CD but a first local check should be done*

If you want to contribute to the project please use *dev* as base branch.

Use *master* branch **ONLY** for critical bug fixes.

Once done create the **Pull Request** to *dev* branch, if it's a critical bug fix use *staging*.

## Branches

### *dev*

This branch is the main development branch and it's the lowest priority branch under CI.

This branch should always build, sometimes can be necessary break this rule, this is why it's should and not must.
 

### *staging*

This branch is for testing the product before a new release.

This branch is the one used to make PR to *master* so this branch **MUST** build.

### *master*

This branch is the production one.

**This must be used for PR only for critical bug fixes** and always **MUST** build.

Changes to README.md or other markdown files are not priorities so for these changes use *dev* or *staging* and they'll be implemented in the next release.

### *every other branch* except *gh-pages*

You can create any branch you want to push any kind of commits.

There are no rules in the CI for all other branches.

Once ready, if you need to implement in the product follow the rules above.

# Backward compatibility

Remember to keep the backward compatibility with previous versions, if a changes breaks this rule *must* be discussed.

You can mark as obsolete old methods but they **must** work too. **Deprecating is not breaking**.

---

# Community

Feel free to join the Slack community to talk about the project. It's easier to share ideas if we can talk directly.

[![Slack](https://cdn.brandfolder.io/5H442O3W/as/pl546j-7le8zk-5guop3/Slack_RGB.auto?width=94&height=38)](https://join.slack.com/t/tsparticles/shared_invite/enQtOTcxNTQxNjQ4NzkxLWE2MTZhZWExMWRmOWI5MTMxNjczOGE1Yjk0MjViYjdkYTUzODM3OTc5MGQ5MjFlODc4MzE0N2Q1OWQxZDc1YzI)

---

Happy coding to everyone!