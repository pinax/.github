# Community Plan

Table of Contents

* [Pinax Community Plan](#pinax-community-plan)
  * [Inspiration](#inspiration) 
  * [Goals of the Pinax Community Plan](#goals-of-the-pinax-community-plan) 
  * [Things to Avoid](#things-to-avoid) 
* [Communication Channels](#communication-channels)
  * [Global Community Health File Repo](#global-community-health-file-repo)
  * [README.md](#readmemd) 
  * [Global Documentation Website](#global-documentation-website) 
  * [Wiki](#wiki)
  * [Blog Posts](#blog-posts) 
* [Community Files](#community-files) 
  * [Community Files in Individual Repos](#community-files-in-individual-repos) 
  * [Global Community Health File Repo](#global-community-health-file-repo) 
* [Global Community Health File Repo Files](#global-community-health-file-repo-files)
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

## Pinax Community Plan

### Inspiration

The Pinax Community Plan was inspired by a talk by Hynek Schlawak entitled [Maintaining a Project When It's Not Your Job](https://speakerdeck.com/hynek/maintaining-a-python-project-when-its-not-your-job). According to Hynek, ideally, using and contributing to a project should be as straightforward as  possible, so that the maintainer becomes involved as late in the process as possible. Otherwise, a failure has happened in the process.

### Goals of the Pinax Community Plan

We strive for clarity, standardization, and discoverability anytime possible. This makes it easier to maintain Pinax and easier to onboard newcomers.

In a nutshell, the Pinax Community Plan should:
1. Help community members find what they need
2. Make it as easy as possible to get started using and contributing to Pinax
3. Increase engagement

### Things to Avoid

* [Tribal knowledge](https://en.wikipedia.org/wiki/Tribal_knowledge) (unwritten knowledge that may be known among members of the "tribe", but unknown to outsiders): knowledge should be documented
* Duplication: there should be one source of truth
* Random location: information should be strategically located

## Communication Channels

### Global Community Health File Repo 

During the 20.XX release, a new [global community health file repo](https://github.com/pinax/.github) was created.

The existing `CODE_OF_CONDUCT.md` and revised `CONTRIBUTING.md` were moved to this repo. New `SUPPORT.md`, `ISSUE_TEMPLATE.md`, `PULL_REQUEST_TEMPLATE.md`, `MAINTAINERS.md`, and `RELEASE.md` were created.

The `CONTRIBUTING.md` files were deleted from individual repos.

The global community health file repo provides some beneficial, built-in functionality
* GitHub will automatically show users popup messages featuring links to some of these files; for example, links to the `CODE_OF_CONDUCT.md` and `CONTRIBUTING.md` files may be shown to first-time contributors

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

### Global Documentation Website

### Wiki

The [Pinax Wiki](https://github.com/pinax/pinax/wiki) contains historical release plans. 

### Blog Posts

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
