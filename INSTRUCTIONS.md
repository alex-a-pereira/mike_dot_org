# What will this app do?
We're making a super simple "blog". No users/authentication or anything (yet).

## MVC (model view controller)

We needs to have CRUD operations (create, read, update, delete) for the following types of data:
1. Posts
  - title
  - body
  - likes (number)
  - comments (a post can have many comments)
2. Comments
  - post (a comment exists on ONLY one post)
  - body
  - likes


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

# Check out what I've already done!

after installing, you'll need to run your local serve

```
rails s
```

you can now navigate to `http://localhost:3000/posts` to see what posts exist in the database already.
There will be NONE!! you'll have to POST data to `http://localhost:3000/posts` in order to create some data.


# Create your first MVC!
I've already created the Posts model and controller.

However, the Post model does not have any reference to comments! we'll need to:
1. create the Comment resource
2. run migrations for comment resource
3. add a has_many relationship on Post
4. add a has_one relationship on Comment
5. create migration to add `post` to Comment table
6. run migrations!
