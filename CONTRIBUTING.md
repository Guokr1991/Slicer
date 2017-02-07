Contributing to Slicer
======================

There are many ways to contribute to Slicer, with varying levels of effort.  Do try to
look through the documentation first if something is unclear, and let us know how we can
do better.

  * Ask a question on the [slicer-devel email list](http://massmail.spl.harvard.edu/mailman/listinfo/slicer-devel)
  * Submit a feature request or bug, or add to the discussion on the [Slicer issue tracker](https://github.com/Slicer/Slicer/issues)
  * Submit a [Pull Request](https://github.com/Radiomics/Slicer/pulls) to improve Slicer or its documentation

We encourage a range of Pull Requests, from patches that include passing tests and
documentation, all the way down to half-baked ideas that launch discussions.

The PR Process, Circle CI, and Related Gotchas
----------------------------------------------

#### How to submit a PR ?

If you are new to Slicer development and you don't have push access to the Slicer
repository, here are the steps:

1. [Fork and clone](https://help.github.com/articles/fork-a-repo/) the repository.
3. Create a branch.
4. [Push](https://help.github.com/articles/pushing-to-a-remote/) the branch to your GitHub fork.
5. Create a [Pull Request](https://github.com/Slicer/Slicer/pulls).

This corresponds to the `Fork & Pull Model` mentioned in the [GitHub flow](https://guides.github.com/introduction/flow/index.html)
guides.

If you have push access to Slicer repository, you could simply push your branch
into the main repository and create a [Pull Request](https://github.com/Slicer/Slicer/pulls). This corresponds to the
`Shared Repository Model` and will facilitate other developers to checkout your
topic without having to [configure a remote](https://help.github.com/articles/configuring-a-remote-for-a-fork/).
It will also simplify the workflow when you are _co-developing_ a branch.

When submitting a PR, make sure to add a `Cc: @Slicer/developers` comment to notify Slicer
developers of your awesome contributions. Based on the
comments posted by the reviewers, you may have to revisit your patches.

#### How to integrate a PR ?

Getting your contributions integrated is relatively straightforward, here
is the checklist:

* All tests pass
* Consensus is reached. This usually means that at least two reviewers added a `LGTM` comment
and a reasonable amount of time passed without anyone objecting. `LGTM` is an
acronym for _Looks Good to Me_.

Next, there are two scenarios:
* You do NOT have push access: A Slicer core developer will integrate your PR.
* You have push access: Simply click on the "Merge pull request" button.

Then, click on the "Delete branch" button that appears afterward.

#### Automatic testing of pull requests

Every pull request is tested automatically using CircleCI each time you push a
commit to it. The Github UI will restrict users from merging pull requests until
the CI build has returned with a successful result indicating that all tests have
passed and there were no problems detected by the linter.

