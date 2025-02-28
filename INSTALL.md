# Installation
## Minimum requirements
We are using strict requirements in the composer file, to make sure compatibility follows from the composer requirements. When you have questions regarding compatibility, install the extension via composer. If it works, it is because it is compatible. If it does not work, it is because it is not compatible. When a new version of Magento comes out, the composer command fails, while you think it should actually work, open a support ticket so we can look into this.

## Instructions for using composer
Use composer to install this extension. First make sure that Magento is installed via composer, and that there is a valid `composer.json` file present.

Next, install our module using the following command:

    composer require yireo/magento2-googletagmanager2

Next, install the new module into Magento itself:

    ./bin/magento module:enable Yireo_GoogleTagManager2
    ./bin/magento setup:upgrade

Check whether the module is succesfully installed in **Admin > Stores >
Configuration > Advanced > Advanced**.

Done.

## Instructions for manual copy
We recommend `composer` to install this package. If you want a manual copy instead, these are the steps. However, please note that we do NOT recommend you to do this.

* Upload the files in the `source/` folder to the folder `app/code/Yireo/GoogleTagManager2` of your site
* Run `php -f bin/magento module:enable Yireo_GoogleTagManager2`
* Run `php -f bin/magento setup:upgrade`
* Flush the Magento cache
* Configure settings under `Stores > Configuration > Sales > Yireo GoogleTagManager`
* Done

## Removing the extension
If you are not the person having added this extension, we very strongly recommend you to have a technical person look into the deinstallation of our module. Deinstalling Magento modules is a technical matter, peanuts for a developer and our extension is not different in any way.

If you have installed this extension via `composer`, simply follow the `composer` procedure again:

    composer remove yireo/magento2-googletagmanager2

If you have copied files to `app/code/Yireo/GoogleTagManager2`, remove them.

Next, follow your deployment procedure to copy changes to your live site. Theoretically, you can modify the `core_config_data` configuration table to remove configuration values from there. Note that Magento does not offer a solid uninstall procedure for this anyway.
