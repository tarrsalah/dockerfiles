compose=docker-compose exec -T web

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

# docker
DOCKERPS=docker ps -aq
docker-clean:
	docker stop `$(DOCKERPS)`

docker-composer-up:
	docker-compose up

docker-composer-down:
	docker-compose down
