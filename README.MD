CriteoConnectorBundle
=====================

Criteo Connector for Akeneo PIM >= 1.5

This connector allow you to export your products into XML for Criteo.

## Requirements

* Akeneo PIM >= 1.5

## Connector installation on Akeneo PIM

If it's not already done, install [Akeneo PIM](https://github.com/akeneo/pim-community-standard).

Get composer (with command line):
```console
$ cd /my/pim/installation/dir
$ curl -sS https://getcomposer.org/installer | php
```

Then, install DnD-CriteoConnectorBundle with composer:

In your ```composer.json```, add the following code:

* In `require`:

```json
{
    "agencednd/criteo-connector-bundle": "1.0.*"
}
```

Next, enter the following command line:
```console
$php composer.phar require agencednd/criteo-connector-bundle
```

Enable the bundle in ```app/AppKernel.php``` file, in the ```registerBundles``` function, before the line ```return $bundles```:
```php
$bundles[] = new Dnd\Bundle\CriteoConnectorBundle\DndCriteoConnectorBundle();
```

## Configuration

###### Create symlink for your images

If you manage your images in the PIM, **you must create a symlink of the _app/file_storage folder_ into the _web folder_** :
```console
$ ln -s /my/pim/installation/dir/web/file_storage /my/pim/installation/dir/app/file_storage
```

###### Export

* Go to _Spread_ > _Export profiles_ and then create your _CriteoConnectorBundle_ export products for Criteo profile
* Map your attributes to Criteo attributes (leave empty if you don't use one of them, see this [Article](http://support.datafeedwatch.com/hc/en-us/articles/200106112-Criteo) to know the required attributes)
* You need to have products complete at 100%. Only them will be exported.
## About us
Founded by lovers of innovation and design, [Agence Dn'D] (http://www.dnd.fr) assists companies in the creation and development of customized digital (open source) solutions for web and E-commerce since 2004.