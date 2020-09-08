# Install

## System Dependencies
have `ruby '2.6.3'` installed on your system
have `sqlite3` installed on your system

## Requirements
```bash
bundle install --path vendor/bundle
```

## Database
```bash
# create the sqlite3 database
rails db:create
# run the initial migrations
rails db:migrate
```
