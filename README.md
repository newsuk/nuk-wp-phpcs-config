### NUK WP PHPCS config

This library contains WordPress VIP PHPCS configuration for NewsUK plugins and themes.

## Installation

Run the following command in terminal:
```bash
composer require --dev newsuk/nuk-wp-phpcs
```

Create a `phpcs.xml.dist` file in your project and add the following:
```xml
<?xml version="1.0"?>
<ruleset name="NewsUK WP PHPCS Rules">
	<rule ref="NewsUK"/>
</ruleset>
```
