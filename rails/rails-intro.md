# Introduction to Ruby on Rails Development

> **Ruby on Rails**, or **Rails**, is a server-side web application framework written in `Ruby` under the MIT License. Rails is a model–view–controller (MVC) framework, providing default structures for a database, a web service, and web pages. It encourages and facilitates the use of web standards such as JSON or XML for data transfer, HTML, CSS and JavaScript for user interfacing.

---

## Links & Resources

- [Rails Website](https://rubyonrails.org/)
- [Getting Started Guide](https://guides.rubyonrails.org/getting_started.html)

---

## Prerequisites

- ruby
  - `ruby --version`
- sqlite3
  - `sqlite3 --version`
- ruby gems
  - `gem --version`
- rails
  - `rails --version`

---

## Create a New Rails Project

```bash
rails new <myproject>
cd <myproject>
rails server
```

### Project Structure

| File/Folder | Purpose |
|:-----------:|:------- |
| app/        | Contains the controllers, models, views, helpers, mailers, channels, jobs, and assets for your application. You'll focus on this folder for the remainder of this guide. |
| bin/        | Contains the rails script that starts your app and can contain other scripts you use to setup, update, deploy, or run your application. |
| config/     | Configure your application's routes, database, and more. |
| config.ru   | Rack configuration for Rack based servers used to start the application. |
| db/         | Contains your current database schema, as well as the database migrations. |
| Gemfile
Gemfile.lock  | These files allow you to specify what gem dependencies are needed for your Rails application. These files are used by the Bundler gem. |
| lib/        | Extended modules for your application. |
| log/        | Application log files. |
| package.json | This file allows you to specify what npm dependencies are needed for your Rails application. This file is used by Yarn. |
| public/     | The only folder seen by the world as-is. Contains static files and compiled assets. |
| Rakefile    | This file locates and loads tasks that can be run from the command line. The task definitions are defined throughout the components of Rails. Rather than changing Rakefile, you should add your own tasks by adding files to the lib/tasks directory of your application. |
| storage/    | Active Storage files for Disk Service. |
| test/       | Unit tests, fixtures, and other test apparatus. |
| tmp/        | Temporary files (like cache and pid files). |
| vendor      | A place for all third-party code. In a typical Rails application this includes vendored gems. |
| .ruby-version | This file contains the default Ruby version. |

---
