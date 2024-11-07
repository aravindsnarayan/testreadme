# Fairgate V4

This project is a Symfony 6.4 application.

## Project Overview

Fairgate V4 is a comprehensive application built using the Symfony framework (version 6.4).  It leverages various Symfony components and third-party bundles to provide a robust and feature-rich platform.

## Technologies Used

**Backend:**

* Symfony 6.4
* Doctrine ORM/DBAL
* Various Symfony Bundles (see below)

**Frontend:**

* Gulp for task automation
* Sass for CSS pre-processing
* PostCSS with Autoprefixer and CSSNano for CSS optimization
* TypeScript for JavaScript development
* Sourcemaps for debugging

## Dependencies

The project utilizes the following key dependencies managed by Composer:

* **Symfony Components:**  `symfony/framework-bundle`, `symfony/console`, `symfony/doctrine-messenger`, `symfony/dotenv`, `symfony/form`, `symfony/http-client`, `symfony/mailer`, `symfony/security-bundle`, `symfony/twig-bundle`, and many more.
* **Doctrine:** `doctrine/orm`, `doctrine/doctrine-bundle`, `doctrine/doctrine-migrations-bundle`
* **Third-party Bundles:** `friendsofsymfony/rest-bundle`, `nelmio/api-doc-bundle`, `gos/web-socket-bundle`, `knplabs/knp-snappy-bundle`, and others.  (See `composer.json` for a complete list.)

The project also uses npm for frontend dependencies:

* `gulp`, `sass`, `postcss`, `autoprefixer`, `cssnano`, `typescript`, and others. (See `package.json` for a complete list.)


## Getting Started

**Prerequisites:**

* **Operating System:** Linux (Ubuntu recommended) or Windows with WSL2 (Ubuntu recommended)
* **Software:** Docker Engine with docker compose, IDE (e.g., PHPStorm recommended)

**Step-by-Step Setup:**

1. **Create Project Directory:**
   ```bash
   mkdir fairgate_project  # Creates a directory named fairgate_project
   cd fairgate_project     # Changes the current working directory to fairgate_project
   ```

2. **Clone Repositories:**
   ```bash
   git clone https://github.com/Fairgate/fairgate_v4.git  # Clones the main Fairgate V4 repository
   git clone https://github.com/Fairgate/fairgate_admin.git # Clones the Fairgate admin repository
   ```

3. **Download and Extract Zip File:** Download  `fairgate_setup.zip` from [link](https://pitsolutions-my.sharepoint.com/:u:/p/aravind_sn/Ec8Ps7iepZFJvxPxhT4WJuoB8_XoQ2mM-g2tLBI4NofXWA) and extract it to the project directory.  This zip file contains Docker Compose configuration and other setup files.

4. **Run Docker Containers:**
   ```bash
   docker compose up -d  # Starts the Docker containers (fairgate-web, fairgate-rabbitmq, fairgate-redis) in detached mode (background)
   ```

5. **Install Dependencies:**
   ```bash
   docker exec -it fairgate-web /bin/bash  # Opens a bash shell inside the running fairgate-web container.
   cd fairgate_v4                         # Changes the working directory to the Fairgate V4 project directory.
   cp ../fairgate_setup/v4/.env.local.php .env.local.php # Copies the local environment configuration file for Fairgate V4.
   composer install                        # Installs the project dependencies using Composer.
   cd ../fairgate_admin                    # Changes the working directory to the Fairgate admin project directory.
   cp ../fairgate_setup/admin/.env.local.php .env.local.php # Copies the local environment configuration file for the Fairgate admin panel.
   composer install                        # Installs the admin panel dependencies using Composer.
   ```

6. **Access the Solution:**
   * Backend: `http://localhost:8080/fruitss/backend/signin`
   * Admin: `http://localhost:8081/signin`

7. **Git Configuration (optional):** This command prevents git from tracking file permission changes.
   ```bash
   git config --global core.filemode false
   ```

## Contributing

(Contribution guidelines would go here.)


## License

(License information would go here.)
