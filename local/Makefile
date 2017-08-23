.PHONY: up
up:
	docker-compose up -d

.PHONY: logs
logs:
	docker-compose logs -f

.PHONY: stop
stop:
	docker-compose stop

.PHONY: down
down:
	docker-compose down

.PHONY: migrate
migrate:
	docker-compose exec api-php sh -c 'cd /var/www && php cli.php migrations:migrate -n'
	docker-compose exec nns /nns -migration file:///migration