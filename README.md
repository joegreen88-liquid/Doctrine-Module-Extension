SwissEngine\Tools\Doctrine\Extension
===============
This small module aims at providing a simple way to add a few features (seamlessly) to the doctrine CLI tool (ZF2) such as the ability to specify the entity manager we want to use optionally.

`php public/index.php orm:validate-schema --em=orm_custom`

Installation
------------

Suggested installation method is through [composer](http://getcomposer.org/):

```php
php composer.phar require joegreen88-liquid/doctrine-module-extension:~1.0
```

Setup
-----

If you use Zend Framework 2, you can now enable this module in your application by adding it to `config/application.config.php` as `SwissEngine\Tools\Doctrine\Extension`.

Just make sure, in order for this to work, you have your doctrine factories set in your config file.
```php
[
    'service_manager' => [
        'factories' => [
            'doctrine.entitymanager.orm_custom' => new \DoctrineORMModule\Service\EntityManagerFactory('orm_custom'),
        ],
    ]
];
```
