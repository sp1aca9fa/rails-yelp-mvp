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
- Bootstrap (for styling)
- Simple Form (for form handling)
- RSpec (for testing)

## Data Model

- **Restaurant**
  - name
  - address
  - phone_number
  - category

- **Review**
  - content
  - rating
  - belongs to a restaurant

## How It Works

- Restaurants and reviews are connected through Active Record associations
- Reviews are nested under restaurants using RESTful routing
- Validations ensure data integrity (e.g., rating range, required fields)
- Forms are handled using Simple Form for cleaner view code

## Setup

git clone <your-repo-url>
cd rails-yelp-mvp
bundle install
rails db:create db:migrate db:seed
rails server

Run tests:
rspec

Open in your browser:
http://localhost:3000/restaurants

## Learnings

- Designing relational data models in Rails
- Implementing associations (has_many / belongs_to)
- Using nested resources and routes
- Validating user input at the model level
- Writing and running tests with RSpec
- Structuring multi-model Rails applications

## Notes

This project was built to practice building a relational Rails application with multiple models and user-driven data.
