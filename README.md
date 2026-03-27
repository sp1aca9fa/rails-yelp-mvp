# Rails Yelp MVP

A Yelp-style web application built with Ruby on Rails where users can browse restaurants and leave reviews.

## Features

- View a list of restaurants
- Add new restaurants
- View restaurant details
- Add reviews to restaurants
- Display reviews associated with each restaurant

## Tech Stack

- Ruby on Rails
- Active Record (ORM)
- ERB (Embedded Ruby)
- Bootstrap 5 (via CDN)
- Simple Form (for form handling)

## Data Model

- **Restaurant**
  - name
  - address
  - phone_number
  - category *(must be one of: chinese, italian, japanese, french, belgian)*

- **Review**
  - content
  - rating *(integer, 0–5)*
  - belongs to a restaurant

## How It Works

- Restaurants and reviews are connected through Active Record associations
- Reviews are nested under restaurants using RESTful routing
- Validations ensure data integrity (e.g., rating range 0–5, required fields, category allowlist)
- Forms are handled using Simple Form for cleaner view code

## Setup

```bash
git clone https://github.com/sp1aca9fa/rails-yelp-mvp.git
cd rails-yelp-mvp
bundle install
rails db:create db:migrate db:seed
rails server
```

Open in your browser:
http://localhost:3000

## Learnings

- Designing relational data models in Rails
- Implementing associations (has_many / belongs_to)
- Using nested resources and routes
- Validating user input at the model level
- Structuring multi-model Rails applications

## Notes

This project is a solution to a Le Wagon bootcamp coding challenge. The purpose was to practice building a relational Rails application with multiple models.
