# Secret Santa - Vitor Hugo Águila Oliveira

This app sort people on Secret Santa

## Installation

The first please install docker and docker-compose:

```bash
https://www.docker.com/community-edition
```

To run the application, first you need to clone the project to you machine by:

```bash
git clone git@github.com:vitorhao/appsecretsanta.git
```

Enter to the new directory created:

```bash
cd app_secret_santa
```

Build the project with Docker

```bash
docker-compose build
```


### Installing gems

To install all the gems that application needs, run:

```bash
docker-compose run --rm app bundle install
```

## Database

To init the database, please run:

```
docker-compose run --rm app bundle exec rails db:create db:migrate
```

This will create the database and run all peding migrations.



### Running the app

Run app in docker-compose:

```bash
docker-compose up
```


## Tests

To run our tests, just run `rspec` command in application root directory.

Controllers tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/controllers
```


Factories tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/factories
```


Helpers tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/helpers
```


Jobs tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/jobs
```


Models tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/models
```


Services tests rspec:

```bash
docker-compose run --rm app bundle exec rspec spec/services
```
