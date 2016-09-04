compose = docker-compose exec -T web

# drush
drush-cc-all:
	$(compose) drush cc all
drush-cc-css-js:
	$(compose) drush cc css-js
drush-cc-theme-registry:
	$(compose) drush cc theme-registry
drush-en:
	$(compose) drush en $(m) -y
drush-dl:
	$(compose) drush dl $(m) -y
