# Ribote Drupal distribution

This is a Drupal Profile aiming for a minimalist and neutral approach. 

## Usage

```
composer create-project daille-daille/ribote-project MY_PROJECT --stability dev --no-interaction
```

## Installing Drupal

You should update the `drush/drush.yml` with your values.
Then install drupal using drush:
```shell
drush si ribote \
  install_configure_form.enable_update_status_emails=NULL \
  install_configure_form.enable_update_status_module=false \
  install_configure_form.date_default_timezone=Europe/France \
  install_configure_form.site_default_country=FR
```
