# TwigBootstrapMaker bundle for Symfony 4 & 5

This repository contains TwigBootstrapMaker bundle which helps you create controller skeletons and templates based on [AdminLTE bundle](https://github.com/kevinpapst/AdminLTEBundle), [TwigBootstrap bundle](https://github.com/sbyaute/TwigBootstrapBundle) and [DataTables bundle](https://github.com/omines/datatables-bundle).

### Minimum requirements

- Symfony 4.4
- PHP 7.1
- Twig 2.0
- [AdminLTE bundle](https://github.com/kevinpapst/AdminLTEBundle)
- [TwigBootstrap bundle](https://github.com/sbyaute/TwigBootstrapBundle)

## Installation with Composer

Installation using composer :

```bash
   composer require sbyaute/TwigBootstrap-Maker
```

Then, enable the bundle by adding it to the list of registered bundles in the `config/bundles.php` file of your project:

```php
<?php

return [
    // ...
    Sbyaute\TwigBootstrapMakerBundle\TwigBootstrapMakerBundle::class => ['all' => true],
];
```

## Usage

This bundle provides several commands under the make: namespace. List them all executing this command:

```sh
php bin/console list make:twigbootstrap

make:twigbootstrap:controller  Creates a new controller class
make:twigbootstrap:crud        Creates TwigBootstrap CRUD for Doctrine entity class
make:twigbootstrap:crudmodal   Creates TwigBootstrap CRUD (modal mode)for Doctrine entity class
```

## Configuration

This bundle doesn't require any configuration. But, you can configure the base layout and several parameters :

```sh
php bin/console config:dump twig_bootstrap_maker

twig_bootstrap_maker:
    base_layout:          '@TwigBootstrap/layout.html.twig'
    skeleton_dir:         .../src/DependencyInjection/../Resources/skeleton/

```

## Translation

The translation messages are located in messages and entity class domain. So yo can update it by using :

```bash
php bin/console translation:update fr --force --output-format=yaml --domain=messages
php bin/console translation:update fr --force --output-format=yaml --domain=[entity class]
```

## License and contributors

Published under the MIT, read the [LICENSE](LICENSE) file for more information.
