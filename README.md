# ActivORM -- Object Relational Mapping based on ActiveRecord

## Features:
* SQL Object - table_name, parse_all, find, insert, update, save
* Searchable - execute SQL where queries
* Associations - belongs_to, has_many, has_one_through

## Still to come:
* Make "where" chainable
* DB validations
* has_many :through

## How to use:
* Extract ZIP file of this repo into the project in which you wish to use it
* In your project, require_relative './ActivORM/activorm'
* Load your SQLite3 Database through 'DBCONNECTION.open(PATH_TO_YOUR_DB_FILE)'
* Query and manipulate data using ActivORM methods

For example:

```ruby
require_relative 'activorm'

class Album < SQLObject
  belongs_to :user, foreign_key: :user_id
  has_many :photos

  finalize!
end
```
