# Ruby Version
  - ruby "3.2.2"

# Rails 7

# How to Run this Project

## first of all stop your postgresql locally using this command
 - sudo systemctl stop postgresql

RUN

1. docker compose build
2. cp .env.example .env
3. docker compose run --rm web bin/rails db:setup
  if docker-entrypoint file permission issue apply this command.
    - chmod +x bin/docker-entrypoint.sh
4. docker compose up

## if you want to run rails console
  - docker compose exec web bin/rails c