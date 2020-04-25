# Maintainers

Table of Contents

* [Development and Community Files](#development-and-community-files) 
  * [Community Files](#community-files) 
  * [Development Files](#development-files) 
* [Pinax Starter Project and App Release](#pinax-starter-project-and-app-release) 
  * [Pinax Starter Projects](#pinax-starter-projects) 
  * [Pinax Apps](#pinax-apps) 
* [High Level Release Process](#high-level-release-process)
  * [Apps Typically Involved](#apps-typically-involved) 
  * [Must Have Improvements](#must-have-improvements) 
  * [Nice to Have Improvements](#nice-to-have-improvements) 
* [How to Know What Changes to Make](#how-to-know-what-changes-to-make)   
  * [Dropping and Adding Support for Python and Django Versions](#dropping-and-adding-support-for-python-and-django-versions) 
  * [Additional Sources of Info](#additional-sources-of-info) 
* [Release Management](#release-management)  
  * [Oversight](#oversight)  
  * [Release Versioning](#release-versioning)
  * [App Versioning](#app-versioning)
* [Release Process](#process)  
  * [Existing Pull Requests and Issues](#existing-pull-requests-and-issues)  
  * [Release Planning Checklist](#release-planning-checklist)  
  * [Testing and Release Checklist](#testing-and-release-checklist)  
  * [Release Pull Request Checklist](#release-pull-request-checklist)  
  * [Documentation, Tutorials, Demos](#documentation-tutorials-demos) 
  * [Community](#community) 
* [Spread the Word](#spread-the-word) 
  * [Stats](#stats) 
  * [Credit](#credit) 
  * [Blog Posts](#blog-posts) 

## Community and Development Files

Many of the files outside of the Pinax project and app folders are configuration and community files used in the development process. 

<!--
For information about JavaScript files, see the JavaScript section.
-->

### Community Files

| Folder/File         | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| README.md           | Project info and instructions                                         |
| LICENSE             |                                                                       |
| CONTRIBUTING.md     |                                                                       |
| AUTHORS             |                                                                       |

### Pinax Starter Project Development Files

| Folder/File                | Description                                                           |
| -------------------------- | --------------------------------------------------------------------- |
| .gitignore                 | Instructs git of files to exclude when pushing files to git repo      |
| Pipfile                    |                                                                       |
| setup.cfg                  |                                                                       |
| update.sh                  | Shell script used to automate commands                                |

### Pinax App Development Files

| Folder/File                | Description                                                           |
| -------------------------- | --------------------------------------------------------------------- |
| .circleci/config.yml       |                                                                       |
| .coveragerc                |                                                                       |
| .gitignore                 | Instructs git of files to exclude when pushing files to git repo      |
| MANIFEST.in                |                                                                       |
| Makefile                   |                                                                       |
| makemigrations.py          |                                                                       |
| runtests.py                |                                                                       |
| setup.py                   |                                                                       |
| tox.ini                    | A Tox config file                                                     |

## Pinax Starter Project and App Release

Pinax code is open-source and can be found in the [Pinax GitHub organization](https://github.com/pinax) account, where Pinax Development takes place. 

Both Pinax starter projects and apps are packaged as tagged releases via GitHub. Tagged releases enable a version of a codebase from a specific point in time to be used.

### Pinax Starter Projects

The contents of each individual starter project branch of the [Pinax starter projects repo](https://github.com/pinax/pinax-starter-projects) becomes a tagged release available on the [Pinax starter projects repo releases page](https://github.com/pinax/pinax-starter-projects/releases).

### Pinax Apps

The contents of each Pinax app repo becomes a tagged release available on the repo releases page and published to the [Python Package Index (PyPi)](https://pypi.org), where developers store packages for reuse by themselves and other developers.

You can search PyPi for all of the [Pinax published packages](https://pypi.org/search/?q=pinax)!

<!--
https://github.com/pinax/pinax-cli/blob/master/pinaxcli/cli.py
https://github.com/pinax/pinax/blob/master/distributions.json
https://github.com/pinax/pinax/blob/master/projects.json
-->

## High Level Release Process

### Apps Typically Involved

* Apps included in last release
* pinax-starter-app
* pinax-cli
* pinax-templates

### Must Have Improvements

* Drop support for Python and Django versions that are no longer officially supported
* Add support for Python and Django versions that are officially supported

### Nice to Have Improvements

* Automation improvements
* Increased [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)-ness.
* CI improvements
* Packaging improvements

## How to Know What Changes to Make

### Dropping and Adding Support for Python and Django Versions

Generally, Pinax supports the officially supported versions of Python and Django. 

For more information, see the following Django docs:
* [Django supported versions chart](https://www.djangoproject.com/download/)
* [Django supported versions policy](https://docs.djangoproject.com/en/dev/internals/release-process/#supported-versions)
* "[Upgrading Django to a newer version](https://docs.djangoproject.com/en/dev/howto/upgrade-version/)"
* "[What Python version should I use with Django?](https://docs.djangoproject.com/en/dev/faq/install/#what-python-version-should-i-use-with-django)" 
* Django release notes "Python Compatibility" section (Example: Release 3.0 "[Python Compatibility](https://docs.djangoproject.com/en/dev/releases/3.0/#python-compatibility)")

### Additional Sources of Info

The Latest GitHub Features
* [GitHub Blog](https://github.blog)  
* [GitHub Changelog](https://github.blog/changelog/) and [GitHub Changelog Twitter](https://twitter.com/GHchangelog)
* [GitHub YouTube](https://www.youtube.com/user/github/videos)

## Release Management

### Oversight

* Update wiki with current and historical release info (See: https://github.com/pinax/pinax/wiki)
* Use a spreadsheet to track updates to individual apps
* Use GitHub milestones within repos, as needed

### Release Versioning

* Pinax releases follow the [CalVer (Calendar Versioning)](https://calver.org/) specification.
* Use `yy.mm` for a limited timeframe
* Otherwise, use `yy.xx`

### App Versioning

* Pinax individual app releases follow the [SemVer (Semantic Versioning)](https://semver.org/) specification.

## Release Process

<!--
### Possibly Deprecated Checklist

Script https://github.com/pinax/pinax/blob/master/check.py can help identify which apps need releases. Be sure to install requirements as specified.

* do a release on GitHub with tag of form `v1.2.3` and release name of `1.2.3`, using the changelog entry for the release notes
* do `git clean -fdx`
* publish to pypi with `python setup.py sdist bdist_wheel upload`

see also https://github.com/pinax/pinax/issues/113
-->

### Existing Pull Requests and Issues

Anytime possible:

* Triage, merge, and close PRs
* Triage and close issues

### Release Planning Checklist

- [ ] Supported versions matrix updated with supported Python and Django versions
- [ ] Dependencies up-to-date, accurate, and documented (`setup.py` and `README.md`)
- [ ] `setup.py` consistent across all apps
- [ ] Consistent use of [SemVer](https://semver.org/) and `Change Log`
- [ ] Ensure that community health files in organization-level, default community health file are up-to-date

### Testing and Release Checklist

- [ ] Make the relevant updates to the app repo, based on the guidance in release plan
- [ ] Make the relevant GitHub Actions and tox updates based on the guidance on the release plan
- [ ] Run the `Makefile` using the `Make` command to test the new supported versions matrix
- [ ] Fix the errors you see in the terminal until you see green at the end of the process
- [ ] Update `Change Log`
- [ ] Update app version number in `setup.py` (Pinax uses [SemVer](https://semver.org/))
- [ ] Create a pull request

### Release Pull Request Checklist

Before publishing
- [ ] Accurate pull request; unit test(s) included, if needed
- [ ] Updated app version number in `setup.py` (Pinax apps use [SemVer](https://semver.org/))
- [ ] Updated `Change Log`, using new app version number

Publishing
- [ ] Ensure `AUTHORS` file is up-to-date (it's possible the process will be automated)
- [ ] Tag the release
- [ ] Package should be automatically published to PyPI or test instance of PyPI by new PyPI GitHub Action anytime a tagged commit is pushed

After publishing
- [ ] App PyPI page renders properly (Note: if you need to re-publish, PyPI will not let you use the existing version number; consider publishing to the test instance of PyPI first)

### Documentation, Tutorials, Demos

Must Have
- [ ] Accurate installation instructions (Apps included in the most recent release should all have basic installation instructions)

Nice to Have
- [ ] Improved usage docs
- [ ] New tutorials
- [ ] New or improved Pinax Starter Project
- [ ] New or improved demo that showcases a Pinax Starter Project or app

### Community

- [ ] Ensure repo has a correct, up-to-date `LICENSE`, if needed (Most Pinax repos include an MIT License; some dates could be incorrect at this time, especially for deprecated or non-app repos)
- [ ] Mark deprecated repos as deprecated, especially in the repo description line
- [ ] Add repo tags (Possible tags: django-project-template, python, django, pinax)

## Spread the Word

Release blog post
* Release stats
* Credit to contributors, including new features
