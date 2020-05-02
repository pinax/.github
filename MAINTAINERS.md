# Maintainers

Table of Contents

* [Pinax Overview](#pinax-overview) 
* [Major Activities](#major-activities) 
  * [Development](#major-activities) 
  * [Release Management](#release-management) 
  * [Technical Community Management](#technical-community-management) 
* [Development Files](#development-files) 
  * [Pinax Starter Project Development Files](#pinax-starter-project-development-files) 
  * [Pinax App Development Files](#pinax-app-project-development-files) 
* [Development Tools Overview](#development-tools-overview) 
  * [Package Architecture](#package-architecture)
  * [Continuous Integration](#continuous-integration)
  * [Supported Versions Matrix Testing](#supported-versions-matrix)
  * [Run Supported Versions Matrix Tests](#run-supported-versions-matrix-tests)
  * [Code Coverage](#code-coverage)
* [Unit Tests](#unit-tests)
  * [Run Unit Tests](#run-unit-tests)
* [Migration](#migration)
  * [Migrate Command](#migrate-command)
* [High Level Community Plan](#high-level-community-plan)
  * [Inspiration](#inspiration) 
  * [Clarity, Standardization, and Discoverability](#clarity-standardization-and-discoverability) 
  * [Goals of the Pinax Community Plan](#goals-of-the-pinax-community-plan) 
  * [Things to Avoid](#things-to-avoid) 
* [Communication Channels](#communication-channels)
  * [Default Community Health File Repo](#default-community-health-file-repo)
  * [Wiki](#wiki)
  * [README.md](#readmemd) 
  * [Blog Posts](#blog-posts) 
  * [GitHub Popups](#github-popups) 
* [Community Files](#community-files) 
  * [Community Files in Individual Repos](#community-files-in-individual-repos) 
  * [Global Community Health File Repo](#global-community-health-file-repo) 
* [Global Community Health File Repo Files](#default-community-health-file-repo-files)
  * [CODE_OF_CONDUCT.md](#code_of_conductmd) 
  * [SUPPORT.md](#supportmd) 
  * [CONTRIBUTING.md](#contributingmd) 
  * [MAINTAINERS.md](#maintainersmd) 
  * [RELEASE.md](#releasemd) 
  * [ISSUE_TEMPLATE/config.yml](#issue_templateconfigyml) 
  * [ISSUE_TEMPLATE/bug_report.md](#issue_templatebug_reportmd) 
  * [ISSUE_TEMPLATE/feature_request.md](#issue_templatefeature_requestmd) 
  * [ISSUE_TEMPLATE/question.md](#issue_templatequestionmd) 
  * [PULL_REQUEST_TEMPLATE.md](#pull_request_templatemd) 
* [Glossary](#glossary)  
  
## Pinax Overview

Pinax code is open-source and can be found in the [Pinax GitHub organization](https://github.com/pinax) account, where Pinax development takes place. 

## Major Activities

### Development

### Release Management

### Technical Community Management
  
## Development Files

Several of the files outside of the Pinax project and app folders are configuration files used in the development process. 

<!--
For information about JavaScript files, see the JavaScript section.
-->

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

## Development Tools Overview

### Package Architecture

Pinax uses a helper class called [django-appconf](https://django-appconf.readthedocs.io) to handle Django app packaging defaults "gracefully."

### Continuous Integration

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

### Code Coverage

[Codecov](https://codecov.io) is used to provide coverage reports. [Coverage](http://coverage.readthedocs.org) is [required to collect coverage metrics](https://github.com/codecov/example-python#how-to-generate-coverage-reports).

### Style, Linting, and Import Sorting

[Flake8](http://flake8.pycqa.org) is used to check style and complexity. Flake8 includes [Doc8](https://github.com/PyCQA/doc8) style checker, [pydocstyle](http://www.pydocstyle.org/) docstring style checker, and [McCabe](http://pypi.python.org/pypi/mccabe) complexity checker.

[Flake8 Quotes](https://github.com/zheller/flake8-quotes), a Flake8 extension for quote linting, is used to enforce double quotes. This is a Pinax design choice.

[isort](http://isort.readthedocs.io) is used to programmatically sort imports.

## Unit Tests

### Run Unit Tests

All apps should include `runtests.py`. 

Run the app's tests:

```shell
    $ python manage.py runtests.py
```

## Migration

### Migrate Command

All apps that have models should include `makemigrations.py`. 

<!--
Instructions are needed for how to use `makemigrations.py`
-->

Run an app's migrations to create database tables:

```shell
    $ python manage.py migrate <app>
```

Run a project's migrations:

```shell
    $ python manage.py migrate
```

## High-Level Community Plan

### Inspiration

The Pinax Community Plan was inspired by a talk by Hynek Schlawak entitled [Maintaining a Project When It's Not Your Job](https://speakerdeck.com/hynek/maintaining-a-python-project-when-its-not-your-job). According to Hynek, ideally, using and contributing to a project should be as straightforward as  possible, so that the maintainer becomes involved as late in the process as possible. Otherwise, a failure has happened in the process.

### Clarity, Standardization, and Discoverability

We strive for clarity, standardization, and discoverability anytime possible. This makes it easier to maintain Pinax, and easier to onboard newcomers.

### Goals of the Pinax Community Plan

1. Help users find what they need
2. Make contributing as easy as possible
3. Increase engagement

### Things to Avoid

* [Tribal knowledge](https://en.wikipedia.org/wiki/Tribal_knowledge): unwritten knowledge that may be known among members of the "tribe", but unknown to outsiders

## Communication Channels

### Default Community Health File Repo 

During the 20.XX release, a new [global community health file repo](https://github.com/pinax/.github) was created.

The existing `CODE_OF_CONDUCT.md` and revised `CONTRIBUTING.md` were moved to this repo. New `SUPPORT.md`, `ISSUE_TEMPLATE.md`, `PULL_REQUEST_TEMPLATE.md`, `MAINTAINERS.md`, and `RELEASE.md` were created.

The `CONTRIBUTING.md` files were deleted from individual repos.

### Wiki

### README.md

The most important Pinax links will be placed at the top of each Pinax `README.md` in an "Important Links" section, including links to files in the global community health file repo. 

The "Important Links" section was inspired by an [example](https://speakerdeck.com/hynek/maintaining-a-python-project-when-its-not-your-job?slide=9) from one of Hyenk's projects.

There are two major benefits of doing this:
1. To improve the discoverability of the most important Pinax links
2. To direct contributors to the new, global `CONTRIBUTING.md`

This `Important Links` Section will tell users and potential contributors where to find:
* Releases
* Global documentation
* App specific documentation
* Support information
* Contributing information
* Current and historical release docs

The `README.md` `Contribute` and `Code of Conduct` section links point to the global community health file repo.

### Blog Posts

### GitHub Popups

## Community Files

### Community Files in Individual Repos

Several of the community files live within individual Pinax project and app repos. These files will be included in any download or installation of that Pinax project or app (See also: `MANIFEST.in`).

| Folder/File         | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| README.md           | Project info and instructions                                         |
| LICENSE             |                                                                       |
| AUTHORS             |                                                                       |

### Global Community Health File Repo

| Folder/File         | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| .github/ISSUE_TEMPLATE/bug_report.md.      |                                                |
| .github/ISSUE_TEMPLATE/config.yml.         |                                                |
| .github/ISSUE_TEMPLATE/feature_request.md  |                                                |
| .github/ISSUE_TEMPLATE/question.md         |                                                |
| .github/PULL_REQUEST_TEMPLATE.md           |                                                |
| CODE_OF_CONDUCT.md                         |                                                |
| CONTRIBUTING.md                            |                                                |
| MAINTAINERS.md                             |                                                |
| README.md                                  |                                                |
| RELEASE.md                                 |                                                |
| SUPPORT.md                                 |                                                |

## Global Community Health File Repo Files
 
### CODE_OF_CONDUCT.md

`CODE_OF_CONDUCT.md`: https://github.com/pinax/.github/blob/master/.github/CODE_OF_CONDUCT.md

### SUPPORT.md

`SUPPORT.md`: https://github.com/pinax/.github/blob/master/.github/SUPPORT.md

### CONTRIBUTING.md

`CONTRIBUTING.md`: https://github.com/pinax/.github/blob/master/CONTRIBUTING.md

### MAINTAINERS.md

`MAINTAINERS.md`: https://github.com/pinax/.github/blob/master/MAINTAINERS.md

### RELEASE.md

`RELEASE.md`: https://github.com/pinax/.github/blob/master/RELEASE.md

### ISSUE_TEMPLATE/config.yml

`config.yml`: https://github.com/pinax/.github/blob/master/.github/ISSUE_TEMPLATE/config.yml

### ISSUE_TEMPLATE/bug_report.md

`bug_report.md`: https://github.com/pinax/.github/blob/master/.github/ISSUE_TEMPLATE/bug_report.md

### ISSUE_TEMPLATE/feature_request.md

`feature_request.md`: https://github.com/pinax/.github/blob/master/.github/ISSUE_TEMPLATE/feature_request.md

### ISSUE_TEMPLATE/question.md

`question.md`: https://github.com/pinax/.github/blob/master/.github/ISSUE_TEMPLATE/question.md

### PULL_REQUEST_TEMPLATE.md

`PULL_REQUEST_TEMPLATE.md`: https://github.com/pinax/.github/blob/master/.github/PULL_REQUEST_TEMPLATE.md

## Glossary

### Tagged Release

Both Pinax starter projects and apps are packaged as tagged releases on GitHub. Tagged releases enable a version of a codebase from a specific point in time to be used.


