
# Composer

## Execute

```
composer validate
composer outdated --minor-only --direct --strict
composer symfony:sync-recipes
```

## Github Action

```
jobs:
  composer:
    - name: Composer Validate
      run: composer validate
```
