# Release

Table of Contents

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
  * [Essential Process to Tag and Publish to PyPI](#essential-process-to-tag-and-publish-to-pypi)  
* [Release Process](#process)  
  * [Release Planning Checklist](#release-planning-checklist)  
  * [Testing and Release Checklist](#testing-and-release-checklist)  
  * [Release Pull Request Checklist](#release-pull-request-checklist)  
  * [Documentation, Tutorials, Demos](#documentation-tutorials-demos) 
  * [Community](#community) 
* [Development Files](#development-files) 
  * [Pinax Starter Project Development Files](#pinax-starter-project-development-files) 
  * [Pinax App Development Files](#pinax-app-project-development-files) 
* [Development Tools Overview](#development-tools-overview) 
  * [Supported Versions Matrix Testing](#supported-versions-matrix)
  * [Run Supported Versions Matrix Tests](#run-supported-versions-matrix-tests)
  * [Continuous Integration](#continuous-integration)
  * [Code Coverage](#code-coverage)
  * [Style, Linting, and Import Sorting](#style-linting-and-import-sorting)
* [Spread the Word](#spread-the-word) 
  * [Stats](#stats) 
  * [Credit](#credit) 
  * [Blog Posts](#blog-posts) 
  
## Pinax Starter Project and App Release

### Pinax Starter Projects

The contents of each individual starter project branch of the [Pinax starter projects repo](https://github.com/pinax/pinax-starter-projects) becomes a tagged release available on the [Pinax starter projects repo releases page](https://github.com/pinax/pinax-starter-projects/releases).

### Pinax Apps

The contents of each Pinax app repo becomes a tagged release available on the repo releases page and published to the [Python Package Index (PyPi)](https://pypi.org), where developers store packages for reuse by themselves and other developers.

You can search PyPI for all of the [Pinax published packages](https://pypi.org/search/?q=pinax)!

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
* Any apps that can be brought up to date

### Must Have Improvements

* Drop support for Python and Django versions that are no longer officially supported
* Add support for Python and Django versions that are officially supported

### Nice to Have Improvements

* Automation improvements
* Increased [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)-ness.
* Continuous Integration (CI) improvements
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

### Essential Process to Tag and Publish to PyPI

<!--
Possibly Deprecated

Script https://github.com/pinax/pinax/blob/master/check.py can help identify which apps need releases. Be sure to install requirements as specified.

* do a release on GitHub with tag of form `v1.2.3` and release name of `1.2.3`, using the changelog entry for the release notes

see also https://github.com/pinax/pinax/issues/113

https://git-scm.com/docs/git-clean
-->

Force removal of untracked files and directories

```bash
$ git clean -fdx
```

Publish to PyPI

```python
$ python setup.py sdist bdist_wheel upload
```

### Release Planning Checklist

- [ ] Supported versions matrix updated with supported Python and Django versions
- [ ] Dependencies up-to-date, accurate, and documented (`setup.py` and `README.md`)
- [ ] `setup.py` consistent across all apps
- [ ] Consistent use of [SemVer](https://semver.org/) and `Change Log`
- [ ] Ensure that community health files in the global community health file are up-to-date

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

## Development Files

Several of the files outside of the Pinax project and app folders are configuration files used in the development process. 

<!--
For information about JavaScript files, see the JavaScript section.
-->

### Pinax Starter Project Development Files

| Folder/File                | Description                                                           |
| -------------------------- | --------------------------------------------------------------------- |
| .gitignore                 | Tells git which files to exclude when work is pushed to GitHub        |
| Pipfile                    |                                                                       |
| setup.cfg                  |                                                                       |
| update.sh                  | A shell script used to automate commands                              |

### Pinax App Development Files

| Folder/File                | Description                                                           |
| -------------------------- | --------------------------------------------------------------------- |
| .circleci/config.yml       |                                                                       |
| .coveragerc                |                                                                       |
| .gitignore                 | Tells git which files to exclude when work is pushed to GitHub        |
| MANIFEST.in                |                                                                       |
| Makefile                   |                                                                       |
| makemigrations.py          |                                                                       |
| runtests.py                |                                                                       |
| setup.py                   |                                                                       |
| tox.ini                    | A tox config file                                                     |

<!--
All apps that have models should include `makemigrations.py`. 
All apps should include `runtests.py`. 
-->

## Development Tools Overview

### Supported Versions Matrix Testing

[tox](https://tox.readthedocs.org) is used to test the supported versions matrix. [detox](https://github.com/tox-dev/detox), a [tox](https://tox.readthedocs.org) plugin used to run tox testenvs in parallel, has been used in Pinax extensively in the past, but will be replaced with [tox parallel mode](https://tox.readthedocs.io/en/latest/example/basic.html#parallel-mode). detox is now an archived project.

### Run Supported Versions Matrix Tests

<!--
If you are preparing an app for a new release, you might also need to test the supported versions matrix. This can usually be done by running the Makefile.
-->

All apps should include a `Makefile`. 

Run the `Makefile`:

```shell
    $ Make
```

### Continuous Integration

### Code Coverage

[Codecov](https://codecov.io) is used to provide coverage reports. [Coverage](http://coverage.readthedocs.org) is [required to collect coverage metrics](https://github.com/codecov/example-python#how-to-generate-coverage-reports).

### Style, Linting, and Import Sorting

[Flake8](http://flake8.pycqa.org) is used to check style and complexity. Flake8 includes [Doc8](https://github.com/PyCQA/doc8) style checker, [pydocstyle](http://www.pydocstyle.org/) docstring style checker, and [McCabe](http://pypi.python.org/pypi/mccabe) complexity checker.

[Flake8 Quotes](https://github.com/zheller/flake8-quotes), a Flake8 extension for quote linting, is used to enforce double quotes. This is a Pinax design choice.

[isort](http://isort.readthedocs.io) is used to programmatically sort imports.

## Spread the Word

Release blog post
* Release stats
* Credit to contributors, including new features
