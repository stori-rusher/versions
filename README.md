# Versions

This repo demonstrates a simple implementation of using Git tags to version a repo and create GitHub releases.

## How it works

The [VERSION](VERSION) file holds the version info. On a push to main, the [tag workflow](.github/workflows/tag.yaml) creates and pushes a git tag with the version. On a successful run of the tag workflow, the [release workflow](.github/workflows/release.yaml) creates a GitHub release with the tag.

## Concepts

### Semantic Versioning

[Semantic Versioning](https://semver.org) is used for the versioning system. A version number is made up of `MAJOR.MINOR.PATCH`. Essentially, a `major` release is created when a breaking change is introduced, a `minor` release is created when a new feature is introduced, and a `patch` release is created for bugfixes, small updates, and anything else.

### Versioning Your Project

Every pull request should update the value in the `VERSION` file. If you are not sure when you should tag your project with version 1.0.0, this version should be when it is ready to be used by your "customer" (another dev, project, or external client).
