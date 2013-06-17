[![Dependencies Status](https://d2xishtp1ojlk0.cloudfront.net/d/9434281)](http://depending.in/IgorTimoshenko/IMTDataGridBundle)

# IMTDataGridBundle #

## Overview ##

This bundle provides a simple integration of the [IMTDataGrid][1] library into
Symfony2. [IMTDataGrid][1] is a library that provides a simple, powerful and
fully customizable tool for generating data-bound grids. This means that you can
use such libraries as [jqGrid][2] in your Symfony2 application.

## Installation ##

### 1. Using Composer (recommended) ###

To install `IMTDataGridBundle` with [Composer][3] just add the following to
your `composer.json` file:

```json
{
    // ...
    "require": {
        // ...
        "imt/data-grid-bundle": "0.9.*"
        // ...
    }
    // ...
}
```

Then, you can install the new dependencies by running [Composer][3]'s update
command from the directory where your `composer.json` file is located:

```sh
$ php composer.phar update imt/data-grid-bundle
```

Now, [Composer][3] will automatically download all required files, and install
them for you. All that is left to do is to update your `AppKernel.php` file, and
register the new bundle:

```php
<?php
// in AppKernel::registerBundles()
$bundles = array(
    // ...
    new IMT\DataGridBundle\IMTDataGridBundle(),
    // ...
);
```

## Usage ##

The bundle provides a new `imt_data_grid.manager` service that returns an
instance of `IMT\DataGrid\Manager\ManagerInterface`. So the only thing to do is
to request the `imt_data_grid.manager` service from the container to get an
instance of `IMT\DataGrid\Manager\ManagerInterface` and start using the
[IMTDataGrid][1] library:

```php
<?php
// ...
$dataGridManager = $container->get('imt_data_grid.manager');
// ...
```

## License ##

This bundle is released under the MIT license. See the complete license in the
bundle:

    Resources/meta/LICENSE

[1]: http://github.com/IgorTimoshenko/IMTDataGrid
[2]: http://github.com/tonytomov/jqGrid
[3]: http://getcomposer.org