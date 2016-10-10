# A Custom [Composer](http://getcomposer.org) Library Installer

This is for PHP package authors to require in their `composer.json`. It will
install their package to the correct location based on the specified package
type.
**Current Supported Package Types**:

> Stable types are marked as **bold**, this means that installation paths
> for those type will not be changed. Any adjustment for those types would
> require creation of brand new type that will cover required changes.

| Framework    | Types
| ---------    | -----
| Yallagroup   | `Yallagroup-module`<br>`Yallagroup-theme`

## Example `composer.json` File

This is an example for a Yallagroup module. The only important parts to set in your
composer.json file are `"type": "yallagroup-module"` which describes what your
package is and `"require": { "mahmouddev/installers": "dev-master" }` which tells composer
to load the custom installers.

```json
{
    "name": "you/ftp",
    "type": "yallagroup-module",
    "require": {
        "mahmouddev/installers": "dev-master"
    }
}
```

This would install your package to the `Modules/Ftp/` folder of a base app route
when a user runs `php composer.phar install`.