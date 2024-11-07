# nuk-wp-phpcs-config

This library contains WordPress VIP PHPCS configuration for NewsUK plugins and themes.

## Architecture

### Project Structure

```text
- .circleci          # CircleCI pipeline configuration files
- .github            # GitHub configuration files
- NewsPress          # NewsPress phpcs rulesets
- NewsUK             # NewsUK phpcs rulesets
```

## Technical Documentation

-   [Package Extensibility](docs/extensibility.md)

## Contribution

More details on how to contribute to this package can be found in the [CONTRIBUTING.md](docs/CONTRIBUTING.md) file.

### Minimal requirements

-   PHP 8.2
-   WordPress 6.2

## Development setup

To build the package

PHP setup

-   `composer install`

## Installation

Composer install:

```bash
composer require --dev newsuk/nuk-wp-phpcs-config
```

## Usage

### Using the ruleset

Create a `phpcs.xml.dist` file in your project and add the following to use `NewsUK` ruleset:

```xml
<?xml version="1.0"?>
<ruleset name="NewsUK WP PHPCS Rules">
	<rule ref="NewsUK"/>
</ruleset>
```

💡 *It is recommended to use the `NewsUK` or `NewsPress` ruleset as it is without customising or overriding rules unless necessary.*

### Usage with Composer
Add the following to `scripts` section in `composer.json` file to run linting.

```json
"lint": "phpcs .",
"lint:fix": "phpcbf .",
```

## Tagging and releasing

The content schema uses Semantic Versioning `semver` for versioning. The package is released using [GitHub Releases](https://docs.github.com/en/github/administering-a-repository/releasing-projects-on-github/about-releases). The release process is automated in Circle CI build step. To create a new release, follow these steps:

-   Update the relevant files with the new version. Commit the updated files.
-   Push the changes to the master branch, by merging the associated pull request
-   Create a release targeting the `master` branch within GitHub.
