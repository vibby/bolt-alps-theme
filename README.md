
This is a bolt Theme, only allowed to be used for 7th Day Adventist Oragnizations

This project in under developement, not ready for a real usage.

In order to use it, you need to install in Bolt some extensions from non-official (from Bolt pov) sources. Follow the steps :

* Install a base Bolt (see https://docs.bolt.cm/2.2/getting-started/installation), and make it works (vhost, database, etc.)

* Edit the file ```./extensions/composer.json``` and Add this content :

```
    […]
    "repositories": {
        […]
        "alps-theme": {
            "type": "vcs",
            "url": "https://github.com/vibby/bolt-alps-theme"
        },
        "alps-extension": {
            "type": "vcs",
            "url": "https://github.com/vibby/bolt-alps-extension"
        },
        "alps": {
            "type": "vcs",
            "url": "https://github.com/vibby/alps"
        },       
    },
    "require": {
        "bolt/sitemap": "^2.2",
        "vibby/bolt-alps-theme": "dev-master"
    },
    […]
```

* Install composer globaly if not done yet : https://getcomposer.org/doc/00-intro.md#globally

* Go to command line and do this : 

```
cd extension
composer update
```

In Bolt admin :

* Edit config file ```app/config/config.yml```, Search theme line and fill it with : ```theme: bolt-alps-theme```

* in extension, go to theme extension and click on «copy to theme folder»

* copy sample content type file in theme file contenttype-sample.yml, to your contenttype.yml

You should be done !
