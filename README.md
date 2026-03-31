# School Management System

A web application for managing teachers, students, and courses built with Ruby on Rails.

## Features

- **Teachers** - Create and manage teaching staff with name and bio
- **Students** - Register students with name and email
- **Courses** - Create courses and assign teachers
- **Enrollments** - Enroll students in multiple courses (many-to-many)
- **Dashboard** - Overview of the school system

## Tech Stack

- Ruby 3.4.9
- Rails 8.1
- PostgreSQL
- Tailwind CSS

## Database Schema

```
teachers: name, bio
students: name, email
courses: title, description, teacher_id (belongs_to teacher)
enrollments: student_id, course_id (join table)
```

### Relationships

- A teacher has many courses
- A student has many courses through enrollments
- A course belongs to a teacher and has many students through enrollments

## Getting Started

### Prerequisites

- Ruby 3.4.9
- PostgreSQL

### Setup

```bash
# Install dependencies
bundle install

# Create and migrate the database
bin/rails db:create db:migrate

# Seed sample data (optional)
bin/rails db:seed

# Start the development server
bin/dev
```

The app will be available at `http://localhost:3000`.

## Routes

| Path | Description |
|------|-------------|
| `/` | Dashboard |
| `/teachers` | Teacher management |
| `/students` | Student management |
| `/courses` | Course management |
