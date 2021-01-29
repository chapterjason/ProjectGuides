
# PHP-CS-Fixer

## Install

```
mkdir -p ./tools/php-cs-fixer
composer require --working-dir=./tools/php-cs-fixer friendsofphp/php-cs-fixer
```

## Update

```console
composer update --working-dir=./tools/php-cs-fixer
```

## Execute

```console
./tools/php-cs-fixer/vendor/bin/php-cs-fixer fix --verbose  
```

## Github Action

```
jobs:
  php-cs-fixer:
    - name: Install
      run: composer install --working-dir=./tools/php-cs-fixer
    - name: PHP-CS-Fixer
      run: ./tools/php-cs-fixer/vendor/bin/php-cs-fixer fix --verbose --diff --dry-run
```

