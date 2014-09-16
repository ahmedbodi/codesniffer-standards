# PHPCS CodeSniffer Standards

Useful CodeSniffer standards to be used with [phpcs](https://github.com/squizlabs/PHP_CodeSniffer).
They go beyond what the original repo offers or include vital fixes.

**These standards are for the phpcs-fixer branch only**. They will only work with this branch of the code sniffer tool.

## Installation
```javascript
{
	"require-dev": {
		"dereuromark/codesniffer-standards": "dev-master"
	}
}
```
if you just want to link the sniffs via `--standard=/path/to/custom/ruleset.xml`.

Otherwise use

	php composer.phar require dereuromark/codesniffer-standards
	phpcs --config-set installed_paths vendor/dereuromark/codesniffer-standards

The second command lets `phpcs` know where to find your new sniffs. Ensure that
you do not overwrite any existing `installed_paths` value.

## Usage
Depending on how you installed the code sniffer changes how you run it.

If you have installed phpcs, you can do the following:

	phpcs --standard=MyStandard /path/to/code

etc.

If not, you can link to the ruleset xml files as shown above.

## Standards

### MyCakePHP
A custom standard with a lot of additional sniffs and the following corrections:
- Doc block indentation correct (same level as methods and attributes for classes)
- LF on Windows are allowed to be \r\n

Dependencies:
- CakePHP standard

### MyCakePHPCore
A custom standard that complies with the official CakePHP coding standards with a lot of additional sniffs and the following corrections:
- LF on Windows are allowed to be \r\n

Dependencies:
- CakePHP standard
- MyCakePHP standard

## Contributing
If you'd like to contribute to the CodeSniffer standards, you can fork the project add features and send pull requests.