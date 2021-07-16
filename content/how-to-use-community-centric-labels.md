# How to use the community-centric labels (e.g. `kind/contributor`, `area/handbook`)
*Author(s): Karsten Wade <kwade@redhat.com> <quaid@iquaid.org>*<br/>
*Date Created: 2021-07-15*<br/>
*Date Updated: N/A*<br/>

This how-to covers using a set of [labels](LINK_TO_PROW_CONTENT_ON_LABELS) that are included in every Operate First community repository by default.
These labels are focused on issues and pull requests related to the Operate First community of users and contributors.

## Overview

As a part of a gitops paradigm, this project uses labels extensively in the gitforge [GitHub](https://github.com/operate-first/).
Labels assist in automation, organization, and visualization for bots, users, and contributors.

These specific labels also serve a purpose for project contributors.
Contributors use this set of labels to mark issues and PRs that are related to an aspect of the community of users and contributors, such as the contribution process, onboarding new contributors, user experience, and so forth.

At the center of this use are three related but distinct labels: `area/community`, `area/contributor`, and `area/user`.

These correspond to the two major groupings of people (users, contributors) who make up the community.
These domain (`area`) labels are connected to a `kind` label to indicate the aspect of community, contributors, and users the issue/PR is related to.

Read on for more details and usage examples.

## List of Labels

| Name | Description | Who can add this label to an issue/PR | Prow Plugin |
| ---- | ----------- | ------------------------------------- | ----------- |
| <a id="area/community" href="#area/community">`area/community`</a> | Indicates an issue/PR is related to the overall community.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="area/contributor" href="#area/contributor">`area/contributor`</a> | Indicates an issue/PR is related to a project platform contributor.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="area/user" href="#area/user">`area/user`</a> | Indicates an issue/PR is related to a project platform user.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/documentation" href="#kind/documentation">`kind/documentation`</a> | Categorizes issue or PR as related to documentation. <br><br> This was previously `docs`, `documentation`, | anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/experience" href="#kind/experience">`kind/experience`</a> | Indicates an issue/PR is related to human interaction and experience.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/governance" href="#kind/governance">`kind/governance`</a> | Indicates an issue/PR is related to governance.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/handbook" href="#kind/handbook">`kind/handbook`</a> | Indicates an issue/PR is related to a handbook.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/marketing" href="#kind/marketing">`kind/marketing`</a> | Indicates an issue/PR is related to marketing.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/metrics" href="#kind/metrics">`kind/metrics`</a> | Indicates an issue/PR is related to metrics.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/news" href="#kind/news">`kind/news`</a> | Indicates an issue/PR is related to project news and outreach.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/onboarding" href="#kind/onboarding">`kind/onboarding`</a> | Indicates an issue/PR is related to onboarding.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |
| <a id="kind/website" href="#kind/website">`kind/website`</a> | Indicates an issue/PR is related to project web presence.| anyone |  [label](https://git.k8s.io/test-infra/prow/plugins/label) |

## Using the labels

In most cases, the minimum requirement is to use at least one `area` label, and at least one `kind` label for the issue/PR bring labeled.

The `area` grouping specifies the domain(s) of the project the issue/PR should be related to.
The `kind` label is used to identify one or more aspects of the domain (area).

### Examples of use

1. A member of the operations team drafts a new blueprint related to the contributor ladder, and labels it `area/contributor` and `kind/handbook` to mark it as something useful for or associated with the Community Handbook.
Another member working on contributor documentation is notified of the newly labeled content and writes up an article to wrap around the blueprint for the Community Handbook.
1. A pull request finishing an Epic is labeled `area/community` and `kind/news` to mark the Epic as ready for a write-up for a social media post, community newsletter, or blog post.
1. A user experience (UX) expert files a series of issues in the `operate-first/operate-first.github.io` repo related to usability and accessibility.
Labeling them `area/user` and `kind/experience`, `kind/website` helps track these issues within the context of all user experience issues/PRs.
1. An issue tracking the refactoring of the `operate-first/common/` repository is labeled `area/contributor` and `kind/handbook` to indicate the Community Handbook may need to be manually updated to reflect these changes.
1. Changes made to the configuration for community metrics web services have the issues/PRs labeled `area/community` and `kind/metrics` for further automation to update related SOPs/documentation.
