
# PHPUnit

## Install

Deprecation issue:

https://github.com/dmaicher/doctrine-test-bundle/issues/129

```console
composer require --dev symfony/test-pack dama/doctrine-test-bundle symfony/panther
```

## Execute

```console
./bin/phpunit --coverage-text
```


## Github Action

```yaml
  - name: "Run tests with phpunit/phpunit"
    run: "./bin/phpunit"

  - name: "Send code coverage report to Codecov.io"
    env:
      CODECOV_TOKEN: "${{ secrets.CODECOV_TOKEN }}"
    run: "bash <(curl -s https://codecov.io/bash) || true"
```
