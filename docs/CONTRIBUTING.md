# Contributing

This package is maintained by the Times CMS team.

## Code Contribution

Developers from outside the team are encouraged to contribute back to this package as part of fix and feature requests. In doing so, developers should ensure their changes adhere to established naming conventions within the package.

## Branching

The `main` branch is the source of truth for the repo. Example: `feat/JIRA-ID-magic-wand` branch should be cut from `main` and used as the base for any development work. Feature and fix branches should be cut from the `main` branch, and follow the `feat/JIRA-ID-*`, `fix/JIRA-ID-*` naming convention. Pull requests for these branches should be targeted at the `main` branch. The branching strategy and the release process is documented [here](https://nidigitalsolutions.jira.com/wiki/spaces/NCP/pages/2329149445/Branching+and+Deployment).

## Commit Messages

Commit messages should follow the Conventional Commits spec, `type(issue-ref): description`

For example, a feature update for issue CPNT-123 that adds a new text box might have a commit message like "feat(CPNT-123): add new text box"
