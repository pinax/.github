# Contributing

Thank you for contributing to Pinax! 

There are many ways to contribute: reporting bugs, requesting features, providing input on issues and pull requests, writing documentation, and submitting code, just to name a few.

## Things We Need Help With

### High Priority Issues

* Make it as easy as possible for new users to get started on any OS (easy install and straightforward docs/tutorial; for Windows, see: https://github.com/pinax/pinax/issues/152)
* Improve our global docs
* Check docs in README.mds to verify accuracy
* Find new ways to automate tasks
* Improve our global community health files (See: https://github.com/pinax/.github/)

### Common Issues

* Find typos
* Find bugs
* Identify and discussing possible new features
* Resolve issues and PRs

### Longterm Issues

* Create tutorials
* Create demos

## Contributing Guidance

### Non-Pull Request (PR) Contributions

Some contributions require a pull request, and others do not.

If you find a bug in a Pinax code base or have a feature request, please open an issue in the repo of that particular Pinax code base.

We also welcome input and discussion in issues and pull requests.

### Pull Request (PR) Contributions

Contributions that will be merged into a code base require a pull request so that a maintainer can review the contribution before merging.

Most people do not have write access to the Pinax organization and will therefore need to fork the Pinax repo they are working on and clone the repo locally.

To fork the repo, click the "Fork" button in the upper right hand corner of the Pinax repo. To clone the repo and change directory, enter your terminal and use the following commands, substituting the real values for the carets and values contained in them.

```bash
$ git clone https://github.com/<your_username>/<pinax_repo_name>
$ cd <pinax_repo_name>
```

Depending on the situation, you might or might not need to create a virtual environment. If needed, do so. A virtual environment is generally required when you are installing packages and want to isolate them from the rest of your computer environment.

You should now be in the master branch of the repo. You can check by using the following command:

```bash
$ git branch
```

If you have forked the repo, it's possible to make your change in the master branch of the fork, and submit a request for the master branch of your fork to be merged into the master branch of the Pinax repo. However, many people prefer to create a separate branch. Leaving the master branch unchanged means that you can create multiple branches off of it.

```bash
$ git checkout -b <new_branch>
```

Keep in mind, that when you create a new branch, you might need to setup the branch like a new project, including installing packages, even if you have done so in the master branch.

When ready, make your change, preferably including any new unit tests your change requires. If you are preparing an app for a new release, you might also need to test the supported versions matrix. See our [App Release Process](https://github.com/pinax/pinax/wiki/App-Release-Process) wiki page for more info.

After any required tests pass and when you are ready, commit your changes. For example:

```bash
$ git add .
$ git commit -m "Your commit message"
```

You can then push your change to your forked repo:

```bash
$ git push origin <new_branch>
```

You can continue to work on the branch, if needed, by making changes locally, adding and committing the changes, then pushing the changes to your branch in the forked repo.

When you are ready to submit a pull request, go to the original Pinax repo you forked. There should be a message identifying your branch and suggesting that you submit a pull request. Click on the "Compare & pull request" button.

Usually, the base branch should be the Pinax repo's master branch and the compare branch will be the branch you created and pushed to your fork. Double check that this is correct and change it if needed.

Create a pull request title and description. 

A box will be checked by default giving Pinax maintainers the ability to edit the pull request. Leave this checked.

Double check your changes

Click "Create pull request"

### Code Style

When writing code for a Pinax project or app, keep in mind:

* Although we do not always follow [PEP 8](http://www.python.org/dev/peps/pep-0008/), PEP 8 is an excellent starting point.
* We do strictly follow the [Django coding style](http://docs.djangoproject.com/en/dev/internals/contributing/#coding-style) outlined in the official Django docs.
