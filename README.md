# README

Having another attempt at getting a docker system set up for developing the Rocktrack application I am thing about.

Currently following the [guides](https://guides.rubyonrails.org/getting_started.html) getting started with dev container, then the Getting Started with Rails.

Following [docker docs use containerised databases](https://docs.docker.com/guides/databases/).

More news when I get some...

## Creating the secrets

The database username and password are stored in `db/username.txt` and `db/password.txt`

Current issue:
```
Caused by:
PG::ConnectionBad: connection to server on socket "/var/run/postgresql/.s.PGSQL.5432" failed: No such file or directory (PG::ConnectionBad)
	Is the server running locally and accepting connections on that socket?
connection to server on socket "/run/postgresql/.s.PGSQL.5432" failed: No such file or directory
	Is the server running locally and accepting connections on that socket?
connection to server on socket "/tmp/.s.PGSQL.5432" failed: No such file or directory
	Is the server running locally and accepting connections on that socket?

Tasks: TOP => db:create
(See full trace by running task with --trace)
```

Looking for
```
There is an issue connecting to your database with your username/password, username: /file/run/db_username.
Please check your database configuration to ensure the username/password are valid.
```

Now looking at [Beginners Guide to Docker for Ruby on Rails, PostgreSQL Development](https://hackernoon.com/beginners-guide-to-docker-for-ruby-on-rails-postgresql-development)

