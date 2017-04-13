# rug-functions-travis

[![Build Status](https://travis-ci.org/atomist-rugs/rug-functions-travis.svg?branch=master)](https://travis-ci.org/atomist-rugs/rug-functions-travis)

Rug functions that hit the [Travis CI][travis-ci] API.  Currently
contains the following Rug functions:

-   `restart-travis-build(org, buildId, token)`
-   `travis-build-rug(owner, repo, version, teamId, gitRef, travisToken, mavenBaseUrl, mavenUser, mavenToken, token)`
-   `travis-enable-repo(owner, repo, org, token)`
-   `travis-disable-repo(owner, repo, org, token)`
-   `travis-encrypt(owner, repo, org, content, token)`

[travis-ci]: https://travis-ci.org/

## Building

To build, test, and install:

```
$ mvn install
```

## Releasing

To create a new release of the project, simply push a tag of the form
`M.N.P` where `M`, `N`, and `P` are integers that form the next
appropriate [semantic version][semver] for release.  For example:

[semver]: http://semver.org

```
$ git tag -a 1.2.3
```

The Travis CI build (see badge at the top of this page) will
automatically create a GitHub release using the tag name for the
release and the comment provided on the annotated tag as the contents
of the release notes.  It will also automatically upload the needed
artifacts.
