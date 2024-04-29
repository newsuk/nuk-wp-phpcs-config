### NUK WP PHPCS config

This library contains WordPress VIP PHPCS configuration for NewsUK plugins and themes.

## Requirements
- PHP 8.2
- WordPress 6.2

## Installation

Composer install:

```bash
composer require --dev newsuk/nuk-wp-phpcs-config
```

## Using the ruleset
Create a `phpcs.xml.dist` file in your project and add the following to use `NewsUK` ruleset:

```xml
<?xml version="1.0"?>
<ruleset name="NewsUK WP PHPCS Rules">
	<rule ref="NewsUK"/>
</ruleset>
```
💡 *It is recommended to use the `NewsUK` or `NewsPress` ruleset as it is without customising or overriding rules unless necessary.*

## Override or add custom rules
You can also override or add custom rules to the config as follows.

```xml
<?xml version="1.0"?>
<ruleset name="NewsUK WP PHPCS Rules">
	<rule ref="NewsUK"/>
	<!-- Overriding the existing text_domain -->
	<rule ref="WordPress.WP.I18n">
		<properties>
			<property name="text_domain" type="array">
				<element value="your_plugin_domain"/>
			</property>
		</properties>
	</rule>
</ruleset>
```
## Composer scripts
Add the following to `scripts` section in `composer.json` file to run linting.

```json
"lint": "phpcs .",
"lint:fix": "phpcbf .",
```