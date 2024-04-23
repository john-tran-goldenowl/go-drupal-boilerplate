# Drupal
This is a boilerplate project for starting new Drupal projects. It includes a basic setup with Docker Compose for running Drupal with Apache, PHP, and MySQL.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)


## Features

- Clean and organized file structure.
- Basic configuration files included.
- Basic directory structure for Drupal modules, themes, profiles, and sites
- Gitignore and editorconfig for consistency.
- Docker Compose setup for local development


## Prerequisites
Before starting the setup process, make sure you have the following installed on your system:
- Docker: [Install Docker](https://docs.docker.com/engine/install/)
- Docker Compose: [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

1. **Configuration:**

    Copy the default settings  into ``./web/sites/default/settings.php``
    
    ```bash
    cp ./web/sites/default/default.settings.php /web/sites/default/settings.php
    ```

2. **Installation:**

    Open a terminal and cd to the folder in which `docker-compose.yml` is saved and run:

    ```bash
    docker-compose up -d --build
    ```
    
    This command will download the necessary Docker images and start the containers in detached mode.
    
    Access Drupal in your browser by navigating to http://localhost:8080.

    Complete the Drupal setup by providing the requested information.

3. **Stopping Drupal:**

    To stop the Drupal containers, run:

    ```bash
    docker-compose down
    ```

    This will stop and remove the containers. The data in the database will persist, and you can start the containers again with `docker-compose up -d` when needed.

## Usage
    
- Develop your themes in themes directory.
- Develop your modules in modules/custom directory.
- Use the `vendor/bin/drush` tool for common Drupal tasks.
- Customize the project based on your specific requirements.

## Configuration

- Customize `/web/sites/default/settings.php` for Drupal configuration.

## Folder Structure

```bash
/drupal-root-path
web/
├── core/
│ ├── assets/
│ ├── autoload.php
│ ├── ...
│
├── modules/
├── profiles/
├── themes/
├── ...
│
├── sites/
│ ├── default/
│ │ ├── files/
│ │ ├── settings.php
│ │ ├── ...
│
vendor/
.gitignore
.editorconfig
composer.json
composer.lock
docker-compose.yml
```

## Core
* [Documentation](https://www.drupal.org/documentation) - Just a main docs of Drupal
* [Drupal Hooks Reference](https://api.drupal.org/api/drupal/core%21core.api.php/group/hooks/10) - Drupal includes many predefined hooks.
* [Drupal Coding Standards](https://www.drupal.org/docs/develop/standards) - The purpose of the Drupal Coding Standards is to create a baseline for collaboration and review within various aspects of the WordPress open source project and community, from core code to themes to modules. 
* [Drupal API](https://api.drupal.org/api/drupal)- Each version of Drupal introduces new APIs and keeps only some of the previous major versions’ APIs.
* [Drupal Modules and Themes](https://www.drupal.org/docs/develop/core-modules-and-themes/core-modules)- Modules are packages of code that extend or modify Drupal's functionality. They can be contributed by the community or custom-built for specific site requirements.
* [Drupal Routing](https://www.drupal.org/docs/drupal-apis/routing-system) - Introduced a new routing system that maps URLs to controller classes, providing a structured way to handle page requests and responses.

