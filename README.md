# DDev PHPUnit Demo

## What is inside of this fork

- Drupal 10.2 support
- joachim-n/drupal-project-contrib-development for easier contrib development
- Simpler setup
- VSCode support

## How to use

- `ddev start`
- Replace `MODULE_NAME` on following with name of your contrib module.
- `ddev composer require drupal/MODULE_NAME`
- `ddev composer drupal-contrib:switch-clone MODULE_NAME`
- `ddev phpunit -v web/modules/contrib/MODULE_NAME`
- `ddev phpunit --group MODULE_NAME`

## Original readmd

See [Running and debugging PHPUnit tests in PHPStorm with DDev and xdebug](https://www.previousnext.com.au/blog/running-and-debugging-phpunit-tests-phpstorm-ddev-and-xdebug) for a video demo covering configuration for running and debugging:

* Unit tests
* Kernel tests
* Functional tests
* FunctionalJavascript tests
* [Drupal Test Traits](https://gitlab.com/weitzman/drupal-test-traits) (ExistingSiteSelenium2DriverTest)
