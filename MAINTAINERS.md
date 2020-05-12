# Maintainers

Table of Contents

* [Major Activities](#major-activities) 
  * [Core Review and Development](#code-review-and-development) 
  * [Release Management](#release-management) 
  * [Technical Community Management](#technical-community-management) 
* [Keeping Track](#keeping-track) 
* [Glossary](#glossary)  

## Major Activities

Pinax maintainers do several different things:
* Code review and development
* Release management
* Technical community management

Here is a bit more information about each activity:

### Code Review and Development

Pinax repos contain issues with feature requests open for debate. From time-to-time, an open-source contributor will open a new issue to suggest a feature or a pull request to add a feature. Pinax maintainers review these PRs and provide feedback, if needed. If the PR is accurate and a good fit for the codebase, the PR will be merged. Pinax maintainers, including several of the original authors, also contribute code to Pinax at times.

Anytime possible:
* Triage, merge, and close PRs
* Triage and close issues

### Release Management

Pinax is made with Python and Django. The Python and Django codebases are improved over time and new releases are published. These new releases often include new features and security measures.

When a new Pinax release happens, the Pinax supported versions matrix is updated to add support for the new versions of Python and Django that are officially supported and drop support for the old versions that are no longer officially supported. The apps included in the Pinax release are then tested against this matrix. Based on the feedback from the tests, changes are made to make the Pinax code compliant with the officially supported versions of Python and Django. 

The apps are then published as tagged releases on GitHub and PyPI.

See the [RELEASES.md](https://github.com/pinax/.github/blob/master/RELEASE.md) for instructions and the [Pinax Wiki](https://github.com/pinax/pinax/wiki) for historical release plans. 

### Technical Community Management

Pinax users and contributors often have questions. They sometimes ask through a GitHub issue in a repo. Pinax issues are configured to give the option of creating a "Question" issue. They might also join the Pinax Slack channel for help. Questions are asked particularly often in the #general, #help, and #community channels. Answer questions, as needed. Other community members will sometimes offer their own insights too.

## Keeping Track

Because the Pinax organization contains around 80 repos, it can be difficult to keep up with the work. Here are a few tips for staying up-to-date:
* If you have access, check the [Pinax GitHub dashboard](https://github.com/orgs/pinax/dashboard) often; this dashboard will show recent activity such as new PRs, issues, comments, and forks
* If you have access, set reminders to review PRs

## Glossary

### Tagged Release

Both Pinax starter projects and apps are packaged as tagged releases on GitHub. Tagged releases enable a version of a codebase from a specific point in time to be used.
