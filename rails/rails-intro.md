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
|:-----------:|:-------:|
|app/        | Contains the controllers, models, views, helpers, mailers, channels, jobs, and assets for your application. You'll focus on this folder for the remainder of this guide. |
|bin/         | Contains the rails script that starts your app and can contain other scripts you use to setup, update, deploy, or run your application. |
|config/      | Configure your application's routes, database, and more. |

---
