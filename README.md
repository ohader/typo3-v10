# TYPO3 v10

## Requirements

* having Docker installed locally (see https://docs.docker.com/get-docker/)
* having DDEV installed locally (see https://ddev.readthedocs.io/en/stable/#installation)

## Install

```
git clone https://github.com/ohader/typo3-v10.git
cd typo3-v10

ddev import-db -f .ddev/backup/db.sql.gz
ddev composer install 
```

* website front-end: https://typo3-v10.ddev.site/
* website back-end: https://typo3-v10.ddev.site/typo3/
  + username: `admin`
  + password: `password`

## DDEV commands

```
ddev start          # starts all relevant Docker containers of this project
ddev stop           # stops all relevant Docker containers of this project
ddev describe       # shows (additional) services used with this project
```

## Side-Notes

Usually Git repositories shall not contain any sensitive information.
This project contains (default) settings in `public/typo3conf/LocalConfiguration.php`
which contains sensitive internal data like `encryptionKey` and database credentials.
