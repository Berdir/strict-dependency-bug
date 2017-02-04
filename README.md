# Steps to reproduce

* composer create-project drupal-composer/drupal-project:8.x-dev dependency-bug --stability dev --no-interaction
* cd dependency-bug/
* rm -rf composer.lock vendor/
* composer require composer/installers:1.0.21
* composer config repositories.demo git https://github.com/Berdir/strict-dependency-bug
* composer require berdir/strict-dependency-bug:^1.0
