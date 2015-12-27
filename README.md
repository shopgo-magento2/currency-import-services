Currency Import Services
========================


#### Contents
*   <a href="#syn">Synopsis</a>
*   <a href="#over">Overview</a>
*   <a href="#install">Installation</a>
*   <a href="#tests">Tests</a>
*   <a href="#contrib">Contributors</a>
*   <a href="#lic">License</a>


<h2 id="syn">Synopsis</h2>

This module adds additional currency rate import services to Magento 2.0.

<h2 id="over">Overview</h2>

With currency import services module, you can import currencies rates with different services such as Yahoo Finance and Google Finance.
This is very important, because Magento 2.0's default and only currency import service WebserviceX tends to go down from time to time.
And sometimes, it returns empty results for some currencies.

<h2 id="install">Installation</h2>

Below, you can find two ways to install the currency import services module. With the release of Magento 2.0, you'll also be able to install modules using the Magento Marketplaces.

### 1. Install via Composer
First, make sure that Composer is installed: https://getcomposer.org/doc/00-intro.md

Add the currency import services module repository's URL:

    php <your Composer install dir>/composer.phar config repositories.shopgo-cis vcs https://github.com/shopgo/currency-import-services

Run Composer require to install it:

    php <your Composer install dir>/composer.phar require shopgo/currency-import-services:~1.0

### 2. Clone the currency-import-services repository
Clone the <a href="https://github.com/shopgo-magento2/currency-import-services" target="_blank">currency-import-services</a> repository using either the HTTPS or SSH protocols.

### 2.1. Copy the code
Create a directory for the currency import services module and copy the cloned repository contents to it:

    mkdir -p <your Magento install dir>/app/code/ShopGo/CurrencyImportServices
    cp -R <currency-import-services clone dir>/* <your Magento install dir>/app/code/ShopGo/CurrencyImportServices

### Update the Magento database and schema
If you added the module to an existing Magento installation, run the following command:

    php <your Magento install dir>/bin/magento setup:upgrade

### Verify the module is installed and enabled
Enter the following command:

    php <your Magento install dir>/bin/magento module:status

The following confirms you installed the module correctly, and that it's enabled:

    example
        List of enabled modules:
        ...
        ShopGo_CurrencyImportServices

<h2 id="tests">Tests</h2>

Unit tests can be found in Magento 2 [app/code/Magento/Directory/Test/Unit](https://github.com/magento/magento2/tree/develop/app/code/Magento/Directory/Test/Unit) directory.

<h2 id="contrib">Contributors</h2>

Ammar (<ammar@shopgo.me>)

<h2 id="lic">License</h2>

[Open Source License](LICENSE.txt)
