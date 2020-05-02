# Maintainers

Table of Contents

* [Overview](#overview) 
* [Community Plan](#community-plan) 
* [Community Files](#community-files) 
  * [Global Community Health File Repo](#global-community-health-file-repo) 
  * [Community Files in Repos](#community-files-in-repos) 
* [Development Files](#development-files) 
  * [Pinax Starter Project Development Files](#pinax-starter-project-development-files) 
  * [Pinax App Development Files](#pinax-app-project-development-files) 
* [Development Tools Overview](#development-tools-overview) 
 * [Package Architecture](#package-architecture)
 * [Continuous Integration](#continuous-integration)
 * [Supported Versions Matrix Testing](#supported-versions-matrix)
 * [Code Coverage](#code-coverage)
* [Commands](#commands)
  * [Migrate](#migrate)
  * [Run Unit Tests](#run-unit-tests)
  * [Run Supported Versions Matrix](#run-supported-versions-matrix)
  
## Overview

## Community Plan

## Community Files

### Global Community Health File Repo

| Folder/File         | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| CONTRIBUTING.md     |                                                                       |

### Community Files in Repos

Several of the files outside of the Pinax project and app folders are community files. 

| Folder/File         | Description                                                           |
| ------------------- | --------------------------------------------------------------------- |
| README.md           | Project info and instructions                                         |
| LICENSE             |                                                                       |
| AUTHORS             |                                                                       |

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

### Code Coverage

[Codecov](https://codecov.io) is used to provide coverage reports. [Coverage](http://coverage.readthedocs.org) is [required to collect coverage metrics](https://github.com/codecov/example-python#how-to-generate-coverage-reports).

### Style, Linting, and Import Sorting

[Flake8](http://flake8.pycqa.org) is used to check style and complexity. Flake8 includes [Doc8](https://github.com/PyCQA/doc8) style checker, [pydocstyle](http://www.pydocstyle.org/) docstring style checker, and [McCabe](http://pypi.python.org/pypi/mccabe) complexity checker.

[Flake8 Quotes](https://github.com/zheller/flake8-quotes), a Flake8 extension for quote linting, is used to enforce double quotes. This is a Pinax design choice.

[isort](http://isort.readthedocs.io) is used to programmatically sort imports.

## Commands

### Migrate

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

### Run Unit Tests

All apps should include `runtests.py`. 

Run the app's tests:

```shell
    $ python manage.py runtests.py
```

### Run Supported Versions Matrix 

If you are preparing an app for a new release, you might also need to test the supported versions matrix. This can usually be done by running the Makefile.

All apps should include `Makefile`. 

Run the `Makefile`:

```shell
    $ Make
```
