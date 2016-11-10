# Dockerfiles


## summary

| image                  | details                     |
|------------------------|-----------------------------|
| [drupal7](./drupal7)   | drupal 7 on lamp (centos 7) |
| [dolibarr](./dolibarr) | dolibarr on lamp (centos 7) |



# drupal7

# dolibarr

The root path to dolibarr installation is
[`./dolibarr/web/dolibarr`](./dolibarr/web/dolibarr).

## pre-installation:

* create `conf.php` in `htdocs/conf` with write permission:

```bash
cp htdocs/conf.php.example htdocs/conf.php
chmod o+w htdocs/conf.php
```

* create `documents` directory in `htdocs` and add the write
permission recursively to that directory:


``` bash
mkdir htdocs/documents
chmod -R o+w htdocs/documents
```

