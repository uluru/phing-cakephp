phing-cakephp
=============

Introduction
------
This is phing configs for CakePHP 2.x project.  
Phing build test [CakePHP](http://cakephp.org/), check code quality (
[phpcs](https://github.com/squizlabs/PHP_CodeSniffer),
 [phpcpd](https://github.com/sebastianbergmann/phpcpd),
 [phpmd](https://github.com/manuelpichler/phpmd)
) and generate [phpdoc](http://www.phpdoc.org/).

Install PHP packages
------
Before place configrations, install PHP packages to your machine.

    pecl install xdebug
    pear channel-discover components.ez.no
    pear channel-discover pear.phpunit.de
    pear channel-discover pear.phpmd.org
    pear channel-discover pear.symfony-project.com
    pear channel-discover pear.symfony.com
    pear channel-discover pecl.php.net
    pear channel-discover pear.pdepend.org
    pear channel-discover pear.netpirates.net
    pear install --alldeps PhpDocumentor
    pear install --alldeps phpunit/phpcpd
    pear install --alldeps phpmd/PHP_PMD
    pear install --alldeps phpunit/PHPUnit

Setup
------
Place XML files to top directory of your CakePHP project.

How to use
------
### Build All ###
We use the command test server by Jenkins.

    phing build

### Build testing and checking only ###
Check your source, before you push. Results log are place to build/logs

    phing build-local

### Testing CakePHP only ###
Only testing, exclude coverage caluculate.

    app/Console/cake test app AllTests
    app/Console/cake test app Model/Foo

License
------
Licensed under The MIT License. Redistributions of files must retain the above copyright notice.

Copyright 2012 [ULURU.CO.,LTD.](http://www.uluru.biz/), https://github.com/uluru
