# Magento 2 Legacy Authentication extension with Prestashop 1.6 password Support

Allows Customer to be logged in using legacy password mechanism (MD5).

For use, if migrating from prestashop 1.6.x to magento 2.

See [gists](https://gist.github.com/ajankuv) for sql queries on exporting the data from prestashop 1.6 for magent 2 export.

## Getting Started

Download the extension as a [ZIP](https://github.com/ajankuv/Sinwashere_LegacyAuthentication/archive/master.zip) file from this repository, unzip the archive and upload the files to `/app/code/Sinwashere/LegacyAuthentication`.

After uploading, run the following [Magento CLI](http://devdocs.magento.com/guides/v2.0/config-guide/cli/config-cli-subcommands.html) commands:

```
bin/magento module:enable Sinwashere_LegacyAuthentication
bin/magento setup:upgrade
bin/magento setup:di:compile
```

These commands will enable the LegacyAuthentication extension, perform necessary database updates, and re-compile your Magento store.

Legacy Authentication can be configured under:

`Magento Admin -> Stores -> Configuration -> Sinwashere -> Legacy Authentication.`

Here you'll be able to enable/disable MD5 authentication, as well as to configure MD5 salt.

## Prestashop 1.6 Magento 2 Support for passwords

`Plugin > AuthenticationPlugin.php`

Line 87 - Here you can add your PS 1.6 "COOKIE_KEY" from config/settings.inc.php in Prestashop 1.6

Once you add your key in this should allow legacy md5 with ps1.6 support.

NOTE: This version is just for ps1.6 migrations, please use the original from [here](https://github.com/sinisa86/Sinwashere_LegacyAuthentication/) by sinisa86 if you need just standard md5 auth.
