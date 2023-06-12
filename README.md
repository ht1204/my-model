# My Model

An exercise to manage a model with RoR

## Requirements
- Install Ruby Version 2.7.6 in your local machine.
- Install rails and run server in project directory:

```
gem install rails
rails console
```
Create a model for `Movie` entity:

```
rails generate model Movie name:text duration:integer year:date rating description image_url:text
```

Create the table:
```
rails db:migrate
```

Create a register, i.e.
```
rails console

m1 = Movie.create(name: "Avengers: Age of Ultron", duration: 141, year: 2015, rating: "PG-13", description: "Marvel Movie", image_url: "https://musicart.xboxlive.com/7/6ec21a00-0000-0000-0000-000000000002/504/image.jpg?w=1920&h=1080")

```

Check that movie was created:
```
irb(main):002:0> Movie.all
  Movie Load (0.4ms)  SELECT "movies".* FROM "movies"
=>
[#<Movie:0x000001de9f7282b8
  id: 1,
  name: "Avengers: Age of Ultron",
  duration: 141,
  year: 2015,
  rating: "PG-13",
  description: "Marvel Movie",
  image_url: "https://musicart.xboxlive.com/7/6ec21a00-0000-0000-0000-000000000002/504/image.jpg?w=1920&h=1080",
  created_at: Sun, 11 Jun 2023 23:45:46.929250000 UTC +00:00,
  updated_at: Sun, 11 Jun 2023 23:45:46.929250000 UTC +00:00>]
```

This should work with any amount of movie registers as you wish.

Enjoy RoR!


Make It Real - Bootcamp
