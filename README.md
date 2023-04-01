# Rails-API-App

## How to Create EVERY Rails API App

## 1. Generate the project.
[List of all available options](https://www.bootrails.com/blog/rails-new-options/)

```sh
rails new my_app --database=postgresql --api --skip-git
```

## 2. RSpec

To ensure these instructions are up to date, if anything goes wrong please [reference the official documentation](https://github.com/rspec/rspec-rails).

Add the following to the Gemfile:

```ruby
group :development, :test do
  gem 'rspec-rails', '~> 6.0.0'
end
```

Next run the following commands:

```sh
$ bundle install
$ rails generate rspec:install
$ bundle binstubs rspec-core
```

## 3. Other Gems

[Pry](https://github.com/pry/pry)  is a runtime developer console and IRB alternative with powerful introspection capabilities. Pry aims to be more than an IRB replacement. It is an attempt to bring REPL driven programming to the Ruby language.

```ruby
gem 'pry', '~> 0.13.1'
```


[Pry-rails](https://github.com/pry/pry-rails). 
Avoid repeating yourself, use pry-rails instead of copying the initializer to every rails project. This is a small gem which causes rails console to open pry. It therefore depends on pry.

```ruby
gem 'pry-rails', :group => :development
```

[Figaro](https://github.com/laserlemon/figaro) was written to make it easy to securely configure Rails applications.
Configuration values often include sensitive information. Figaro strives to be secure by default by encouraging a convention that keeps configuration out of Git.

```ruby
gem 'figaro'
```

```sh
$ bundle install
$ bundle exec figaro install
```
Create a new file ```config/application.yml``` for your environment configuration.


[Annotate](https://makingsenseofrails.dev/how-to-use-the-annotate-gem-c44bfec97d03) gem will add a comment to the top of selected files (models, fixtures, specs) describing the database schema relevant to those files — including field names, index configuration, and foreign keys. It will update these comments automatically whenever you run rails db:migrate.

```ruby
group :development do
  gem 'annotate'
end
```

```sh
$ bundle install
$ bundle exec rails g annotate:install
```
This will generate a rake task in lib/tasks/auto_annotate_models.rake with the default configuration.


## 3. I hope this information is useful to you. Thank you for taking the time to read, RailsReactCombo.
