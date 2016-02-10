Code Contributions
==================

**Code of Conduct** 

The Code of Conduct explains the bare minimum behavior expectations Relevance Lab requires of its contributors.

This project adheres to the [Open Code of Conduct][code-of-conduct]. By participating, you are expected to honor this code.
[code-of-conduct]: http://todogroup.org/opencodeofconduct/#RLCatalyst/kaushik.mukherjee@relevancelab.com


**Issue Contributions** 

When opening new issues or commenting on existing issues please make sure discussions are related to concrete technical issues with the RLCatalyst software.
  Discussion of non-technical topics including subjects like intellectual property, trademark and high level project questions should be directed to support@relevancelab.com


**Branching Strategy**

The central repository will have two branches with infinite lifetime

* master 
* dev 

*Supported Branches* 
For contributions to RLCatalyst create a feature or hot fix branch and make changes. Usage of the branches shall be explained in the following section.


**Code Contributions**

*Step 1: Fork*

$ git clone git@github.com:username/rlcat-core.git
$ cd rlcatalyst
$ git remote add upstream git://github.com/RLOpenCatalyst/core.git

*Step 2: Branch*

Create a feature branch and start hacking:

$ git checkout -b my-feature-branch -t origin/master

*Step 3: Commit*

Make sure git knows your name and email address:

$ git config --global user.name "J. Random User"
$ git config --global user.email "j.random.user@example.com"
Writing good commit logs is important. A commit log should describe what changed and why. Follow these guidelines when writing one:

The first line should be 50 characters or less and contain a short description of the change prefixed with the name of the changed subsystem (e.g. "net: add localAddress and localPort to Socket").
Keep the second line blank.
Wrap all other lines at 72 columns.
A good commit log can look something like this:

subsystem: explaining the commit in one line

Body of commit message is a few lines of text, explaining things
in more detail, possibly giving some background about the issue
being fixed, etc. etc.

The body of the commit message can be several paragraphs, and
please do proper word-wrap and keep columns shorter than about
72 characters or so. That way `git log` will show things
nicely even when it is indented.
The header line should be meaningful; it is what other people see when they run git shortlog or git log --oneline.

Check the output of git log --oneline files_that_you_changed to find out what subsystem (or subsystems) your changes touch.

*Step 4: Rebase*

Use git rebase (not git merge) to sync your work from time to time.

$ git fetch upstream
$ git rebase upstream/master

*Step 5: Tests*

Bug fixes and features should come with tests. Add these tests in the tests directory of the repository.

*Step 6: Push*

$ git push origin my-feature-branch
Pull requests will usually be reviewed within a few days. If there are comments to address, apply your changes in a separate commit and push that to your feature branch. Post a comment in the pull request afterwards; GitHub does not send out notifications when you add commits.

**Code Review**

Each Github pull request will go through 3 step before merge:

1. We will execute our automated test cases against the pull request. If the tests failed the pull request will be rejected with comments provided on the failures.

2. If tests pass, the RLCatalyst engineering team member will do the review of the changes. Technical communication possible via github.com pull request page. When ready, your pull request will be tagged with label Ready For Merge.

3. Your patch will be merged into master including necessary documentation updates.

**Issue Contributions**

RLCatalyst Issue Tracking is handled using Github Issues.

If you are familiar with RLCatalyst and know the repository that is causing you a problem or if you have a feature request on a specific component, you can file an issue in the corresponding GitHub project. All of our Open Source Software can be found in our GitHub organization.

Otherwise you can file your issue in the RLCatalyst project and we will make sure it gets filed against the appropriate project.

To decrease the back and forth in issues, and to help us get to the bottom of them quickly, we use the issue template below. You can copy/paste this template into the issue you are opening and edit it accordingly::

 Version:[Version of the project installed]

 Environment:[Details about the environment such as the Operating System, cookbook details, etc.]

 Scenario:[What you are trying to achieve and you can't?]

 Steps to Reproduce:[If you are filing an issue, what are the things we need to do to reproduce your problem?]

 Expected Result:[What are you expecting to happen as the consequence of the reproduction steps above?]

 Actual Result:[What actually happens after the reproduction steps?]


