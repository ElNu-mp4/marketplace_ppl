# Marketplace PPL

[![PHP](https://img.shields.io/badge/PHP-8.2+-8892bf?logo=php)](https://www.php.net)
[![Laravel](https://img.shields.io/badge/Laravel-12.0-red?logo=laravel)](https://laravel.com)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.4-06b6d4?logo=tailwindcss)](https://tailwindcss.com)
[![Vite](https://img.shields.io/badge/Vite-7.2-646cff?logo=vite)](https://vitejs.dev)
[![Pest](https://img.shields.io/badge/Testing-Pest-blue?logo=pestphp)](https://pestphp.com)

Marketplace PPL is a Laravel marketplace application built as a course assignment to demonstrate full-stack web development capabilities. It implements a realistic multi-role marketplace with seller onboarding, admin approval workflows, and transactional email—showcasing practical Laravel patterns, clean architecture, and modern web development tooling.

## Table of Contents

- [Overview](#overview)
- [Learning Objectives](#learning-objectives)
- [Core Capabilities](#core-capabilities)
- [Built With](#built-with)
- [Repository Structure](#repository-structure)
- [Quick Start](#quick-start)
- [Commands](#commands)
- [Testing](#testing)
- [Technical Highlights](#technical-highlights)

## Overview

Marketplace PPL is a multi-role marketplace application with dedicated seller onboarding, administrative approval workflows, and secure email activation. It models a realistic business process where sellers register, submit required documentation, and await verification before gaining access to platform functionality.

## Learning Objectives

This project demonstrates competency in:

- Full-stack Laravel application architecture and request lifecycle
- Secure role-based authentication and authorization patterns
- Stateful workflow orchestration and business logic implementation
- Database design with migrations, relationships, and seeders
- Form validation and request handling best practices
- Email service integration and transactional workflows
- Modern frontend tooling (Vite, Tailwind CSS, Alpine.js)
- Automated testing with Pest and behavior-driven test design

## Core Capabilities

- Role-based authentication and access control for `admin`, `seller`, and `buyer`
- Seller onboarding form with document uploads, validation, and review status
- Admin dashboard for seller approval, rejection, and activation notifications
- Transactional email workflow using Laravel Mail and mailable classes
- Secure account activation flow with temporary password setup and login handoff
- Responsive UI built with Blade, Tailwind CSS, and Vite asset compilation
- Structured request validation using Laravel form request objects
- Database migrations and seeders for repeatable development setup
- Test-ready architecture with PHPUnit/Pest support

## Built With

- PHP 8.2+
- Laravel 12
- Eloquent ORM
- Blade template engine
- Tailwind CSS
- Vite
- Alpine.js
- Laravel Mail
- Pest for testing

## Repository Structure

- `app/Http/Controllers` – request handling and workflow orchestration
- `app/Http/Requests` – centralized validation logic
- `app/Models` – core domain entities (`User`, `Seller`)
- `app/Mail` – transactional email notifications
- `resources/views` – server-rendered page templates
- `database/migrations` – schema versioning
- `database/seeders` – seeded demo data for evaluation
- `tests` – automated validation and behavior coverage

## Quick Start

1. Clone the repository:

   ```bash
   git clone https://github.com/ElNu-mp4/marketplace_ppl.git
   cd marketplace_ppl
   ```

2. Install PHP dependencies:

   ```bash
   composer install
   ```

3. Install frontend dependencies:

   ```bash
   npm install
   ```

4. Create the environment file and application key:

   ```bash
   copy .env.example .env
   php artisan key:generate
   ```

5. Run database migrations and seed sample data:

   ```bash
   php artisan migrate --seed
   ```

6. Start the development server:

   ```bash
   php artisan serve
   ```

## Commands

Use these repository scripts to streamline setup and development:

- `composer setup` – install dependencies, generate key, migrate database, install npm, build assets
- `npm run dev` – start Vite development server
- `npm run build` – compile frontend assets for production
- `php artisan serve` – launch Laravel development server

## Testing

Execute the test suite to validate behavior and regressions:

```bash
./vendor/bin/pest
```

## Technical Highlights

- **Workflow State Management**: Implements seller approval pipeline with email notifications at each stage
- **Request Validation**: Centralized form request classes with custom validation rules
- **Clean Architecture**: Separation of concerns across controllers, models, requests, and mailable classes
- **Database Relationships**: Eloquent relationships and migrations that model realistic business domains
- **Email Integration**: Laravel Mail with mailable classes for transactional notifications
- **Asset Pipeline**: Vite integration for fast development and optimized production builds
- **Automated Setup**: Composer and npm scripts for repeatable development environment setup
- **Test Coverage**: Pest tests validating authentication, authorization, and workflow behavior


