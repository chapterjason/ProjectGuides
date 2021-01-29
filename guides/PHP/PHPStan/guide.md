
# PHPStan

[PHPStan](https://phpstan.org/user-guide/getting-started)
[PHPStan Symfony Framework extensions and rules](https://github.com/phpstan/phpstan-symfony)
[Doctrine extensions for PHPStan](https://github.com/phpstan/phpstan-doctrine)
[PHPStan PHPUnit extensions and rules](https://github.com/phpstan/phpstan-phpunit)
[Slam PHPStan extensions](https://github.com/Slamdunk/phpstan-extensions)
[TheCodingMachine's additional rules for PHPStan](https://github.com/thecodingmachine/phpstan-strict-rules)
[Rules for detecting usage of deprecated classes, methods, properties, constants and traits.](https://github.com/phpstan/phpstan-deprecation-rules)

## Install

```console
mkdir -p ./tools/phpstan
composer require --working-dir=./tools/phpstan phpstan/phpstan phpstan/phpstan-symfony phpstan/phpstan-phpunit phpstan/phpstan-deprecation-rules phpstan/phpstan-doctrine thecodingmachine/phpstan-strict-rules slam/phpstan-extensions
```

## Update

```console
composer update --working-dir=./tools/phpstan
```

## Execute

```console
./tools/phpstan/vendor/bin/phpstan analyse
```

## Github Action

```
jobs:
  phpstan:
    - name: Install
      run: composer install --working-dir=./tools/phpstan
    - name: PHPStan Static Analysis
      run: ./tools/phpstan/vendor/bin/phpstan analyse --error-format=github
```
