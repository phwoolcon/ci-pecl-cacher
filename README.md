# phwoolcon/ci-pecl-cacher

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Build Status][ico-travis]][link-travis]
[![Total Downloads][ico-downloads]][link-downloads]
[![Software License][ico-license]](LICENSE.md)

PECL installing script with cache for Travis CI

## Install
Via Composer
```bash
$ composer require phwoolcon/ci-pecl-cacher
```

## Usage
Edit `.travis.yml`
```bash
vim .travis.yml
```
To enable cache support:
```yaml
cache:
  directories:
    - $HOME/pecl_cache
```
To install PECL extension:
```yaml
before_install:
  - composer require phwoolcon/ci-pecl-cacher -n
  # Cache till new version
  - vendor/bin/ci-pecl-install swoole
  # Cache and skip version check
  - vendor/bin/ci-pecl-install swoole skip-update
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Security

If you discover any security related issues, please email fishdrowned@gmail.com instead of using the issue tracker.

## Credits

- [Christopher CHEN][link-author]
- [All Contributors][link-contributors]

## License

The Apache License, Version 2.0. Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/phwoolcon/ci-pecl-cacher.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/phwoolcon/ci-pecl-cacher/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/phwoolcon/ci-pecl-cacher.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/phwoolcon/ci-pecl-cacher.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/phwoolcon/ci-pecl-cacher.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/phwoolcon/ci-pecl-cacher
[link-travis]: https://travis-ci.org/phwoolcon/ci-pecl-cacher
[link-scrutinizer]: https://scrutinizer-ci.com/g/phwoolcon/ci-pecl-cacher/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/phwoolcon/ci-pecl-cacher
[link-downloads]: https://packagist.org/packages/phwoolcon/ci-pecl-cacher
[link-author]: https://github.com/Fishdrowned
[link-contributors]: ../../contributors
