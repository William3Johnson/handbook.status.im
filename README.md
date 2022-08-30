# Description

This repository is the source for https://handbook.status.im/.

It is built using [mdBook](https://rust-lang.github.io/mdBook/).

# Development

### GitHub

The simplest way to make changes is by [editing files on GitHub](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files) and [creating Pull Requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

A simple alternative to using the GitHub Web UI is using their [Desktop Application](https://desktop.github.com/).

### Local Build

Clone repository locally using [Git](https://git-scm.com/):
```
git clone https://github.com/status-im/handbook.status.im.git
```
You will need to [install mdBook](https://github.com/rust-lang/mdBook#installation).

To start a server that also builds the page use:
```
cd handbook.status.im
mdbook serve
```
Will expose the built page under http://localhost:3000/.

# Continuous Integration

Two branches are built by [our Jenkins instance](https://ci.infra.status.im/):

* `master` branch is deployed to https://handbook.status.im/ by [CI](https://ci.infra.status.im/job/website/job/handbook.status.im/).
* `develop` branch is deployed to https://dev-handbook.status.im/ by [CI](https://ci.infra.status.im/job/website/job/dev-handbook.status.im/).

PRs should be made for `develop` branch and `master` should be [rebased](https://git-scm.com/book/en/v2/Git-Branching-Rebasing) on `develop` once changes are verified.
