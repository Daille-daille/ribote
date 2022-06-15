# Ribote Drupal distribution

This is a Drupal Profile aiming for a minimalist and neutral approach. 

## Usage

```
composer create-project daille-daille/ribote-project MY_PROJECT --stability dev --no-interaction
```

## Installing Drupal

You should update the `.env` file with your values and add you project url in your /etc/hosts file:
```shell
  echo "127.0.0.1 my-app.local" | sudo tee -a /etc/hosts
```

Then install drupal using drush:
```shell
vendor/bin/drush si ribote \
  install_configure_form.enable_update_status_emails=NULL \
  install_configure_form.enable_update_status_module=false \
  install_configure_form.date_default_timezone=Europe/Paris \
  install_configure_form.site_default_country=FR
```

You can use the php built-in server:
```shell
cd web
php -S my-app.local:8888 ht.router.php
```
