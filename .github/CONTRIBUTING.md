# Contributing to Lyv Platform

Looking to contribute something to Lyv Platform? **Here is how you can help.**

Please take a moment to review this document in order to make the contribution
process easy and effective for everyone involved.

Following these guidelines helps to communicate that you respect the time of the
developers managing and developing this open source project. In return, they
should reciprocate that respect in addressing your issue or assessing patches
and features.


## Code of Conduct

This project and everyone participating in it is governed by the [Code of
Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this
code. Please report unacceptable behavior to [ojoaofernandes@gmail.com](
mailto:ojoaofernandes@gmail.com).


## License

By contributing your code, you agree to license your contribution under the [MIT
License](../LICENSE).


## Using the issue tracker

The [issue tracker](./issues) is the preferred channel for [bug reports](
#bug-reports), [features requests](#feature-requests) and [submitting pull
requests](#pull-requests), but please respect the following restrictions:

* Please **do not** derail or troll issues. Keep the discussion on topic and
respect the opinions of others.

* Please **do not** post comments consisting solely of "+1" or ":thumbsup:".
Use [GitHub's "reactions" feature](https://blog.github.com/2016-03-10-add-reactions-to-pull-requests-issues-and-comments/) instead. We
reserve the right to delete comments which violate this rule.


## Bug reports

A bug is a _demonstrable problem_ that is caused by the code in the repository.
Good bug reports are extremely helpful, so thanks!

Guidelines for bug reports:

1. **validate your implementation** to ensure your problem is not caused by a
simple error in your own code.

2. **Use the GitHub issue search** &mdash; check if the issue has already been
reported.

3. **Check if the issue has been fixed** &mdash; try to reproduce it using the
latest `master` or development branch in the repository.

4. **Isolate the problem** &mdash; ideally create a [reduced test case](
https://css-tricks.com/reduced-test-cases/) and a live example.

A good bug report should not leave others needing to chase you up for more
information. Please try to be as detailed as possible in your report. What is
your environment? What steps will reproduce the issue? What browser(s) and OS
experience the problem? Do other browsers or OS show the bug differently? What
would you expect to be the outcome? All these details will help people to fix
any potential bugs.

Example:

> Short and descriptive example bug report title
>
> A summary of the issue and the browser/OS environment in which it occurs. If
> suitable, include the steps required to reproduce the bug.
>
> 1. This is the first step
> 2. This is the second step
> 3. Further steps, etc.
>
> `<url>` - a link to the reduced test case
>
> Any other information you want to share that is relevant to the issue being
> reported. This might include the lines of code that you have identified as
> causing the bug, and potential solutions (and your opinions on their merits).


## Feature requests

Feature requests are welcome. But take a moment to find out whether your idea
fits with the scope and aims of the project. It is up to *you* to make a strong
case to convince the project's developers of the merits of this feature. Please
provide as much detail and context as possible.


## Pull requests

Good pull requests — patches, improvements, new features — are a fantastic help.
They should remain focused in scope and avoid containing unrelated commits.

**Please ask first** before embarking on any significant pull request (e.g.
implementing features, refactoring code, porting to a different language),
otherwise you risk spending a lot of time working on something that the
project's developers might not want to merge into the project.

Please adhere to the coding guidelines used throughout the project (indentation,
accurate comments, etc.) and any other requirements (such as test coverage).

Similarly, when contributing to Lyv Platform's documentation, you should edit
the documentation source files.

Adhering to the following process is the best way to get your work included in
the project:

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your
fork, and configure the remotes:

  ```bash
  # Clone your fork of the repo into the current directory
  git clone https://github.com/<your-username>/<repository>.git
  # Navigate to the newly cloned directory
  cd <repository>
  # Assign the original repo to a remote called "upstream"
  git remote add upstream https://github.com/lyv-platform/<repository>.git
  ```

2. If you cloned a while ago, get the latest changes from upstream:

  ```bash
  git checkout master
  git pull upstream master
  ```

3. Create a new topic branch (off the main project development branch) to
contain your feature, change, or fix:

  ```bash
  git checkout -b <topic-branch-name>
  ```

4. Commit your changes in logical chunks. Please adhere to these [git commit
message guidelines](
https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) or your
code is unlikely be merged into the main project. Use Git's [interactive rebase
](https://help.github.com/articles/about-git-rebase/) feature to tidy up your
commits before making them public.

5. Locally merge (or rebase) the upstream development branch into your topic
branch:

  ```bash
  git pull [--rebase] upstream master
  ```

6. Push your topic branch up to your fork:

  ```bash
  git push origin <topic-branch-name>
  ```

7. [Open a Pull Request](https://help.github.com/articles/about-pull-requests/)
with a clear title and description against the `master` branch.

---

Thanks,

**Lyv Platform Team :heart:**
