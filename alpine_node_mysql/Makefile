include .env
export

install:
	docker-compose --env-file ./.env  --project-name $(PROJECT_NAME) up -d

uninstall:
	docker-compose --env-file ./.env  --project-name $(PROJECT_NAME) down

run-shell:
	docker exec -it $(PROJECT_NAME)_app_1 zsh

stop:
	docker-compose -p $(PROJECT_NAME) stop

start:
	docker-compose -p $(PROJECT_NAME) start
