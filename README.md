# DDEV PHPUnit Demo

## What is inside of this fork

- Drupal 11.x support
- ARM-architechture support Selenium-Chrome image.
- Simpler setup
- VSCode support

## How to use

- Install [DDEV](https://ddev.readthedocs.io/en/latest/users/install/ddev-installation/)
- `ddev start`
- Replace `MODULE_NAME` on following with name of your contrib module (use admin_toolbar).
- `ddev composer install`

### Adding new modules:

This is work-a-round until following issues are resolved:
- https://github.com/joachim-n/drupal-core-development-project/issues/14
- https://github.com/joachim-n/drupal-core-development-project/pull/28


- `ddev composer require drupal/MODULE_NAME`
- `cd web/modules/contrib; rm -rf MODULE_NAME`
- `git clone git@git.drupal.org:project/MODULE_NAME`

## PHPStan

To analyze using the distributed phpstan.neon.xml file:
```
phpstan web/modules/contrib/MODULE_NAME
```

to get more errors to fix, increase the level
```
phpstan web/modules/contrib/MODULE_NAME -l9
```

## PHPCS

```
ddev phpcs web/modules/contrib/MODULE_NAME
```

## PHPCBF

```
ddev phpcbf web/modules/contrib/MODULE_NAME
```

## CSPell

```
cd web/core
ddev yarn install
ddev yarn run spellcheck ../modules/contrib/MODULE_NAME
```

## ESlint

```
ddev eslint web/modules/contrib/MODULE_NAME
ddev eslint web/modules/contrib/MODULE_NAME --fix
```

## Run PHPUnit tests

- `ddev phpunit web/modules/contrib/MODULE_NAME`
- `ddev phpunit --debug web/modules/contrib/MODULE_NAME`
- `ddev phpunit --group MODULE_NAME`

## Other resources

- https://github.com/justafish/ddev-drupal-core-dev

## Original readmd

See [Running and debugging PHPUnit tests in PHPStorm with DDev and xdebug](https://www.previousnext.com.au/blog/running-and-debugging-phpunit-tests-phpstorm-ddev-and-xdebug) for a video demo covering configuration for running and debugging:

* Unit tests
* Kernel tests
* Functional tests
* FunctionalJavascript tests
* [Drupal Test Traits](https://gitlab.com/weitzman/drupal-test-traits) (ExistingSiteSelenium2DriverTest)
