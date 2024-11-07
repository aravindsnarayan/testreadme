# Fairgate V4

This is a web application built with Symfony 6.4, a powerful PHP framework for web applications. This project follows best practices and utilizes the latest Symfony features to build a scalable and maintainable web application.


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
   ```

3. **Download and Extract Zip File:** Download  `fairgate_v4-setup.zip` from [link](https://pitsolutions.sharepoint.com/:u:/s/ProjectManagement/Agile6_Php/EWQTSnA3KPpBrRbFolOnh1kBlyFNJZKULq07xLYmy1k9qQ) and extract it to the project directory.  This zip file contains Docker Compose configuration and other setup files.

4. **Run Docker Containers:**
   ```bash
   docker compose up -d  # Starts the Docker containers (fairgate-web, fairgate-rabbitmq, fairgate-redis) in detached mode (background)
   ```

5. **Install Dependencies:**
   ```bash
   docker exec -it fairgate-web /bin/bash  # Opens a bash shell inside the running fairgate-web container.
   cd fairgate_v4                         # Changes the working directory to the Fairgate V4 project directory.
   composer install                        # Installs the project dependencies using Composer.
   composer dump-env dev                  # Dumps the .env.local.php file with the current environment variables.
   ```
The generated .env.local.php should be populated with the approprate values.

6. **Access the Solution:**
   * Backend: `http://localhost:8080/fg-standard-club/backend/signin`

7. **Git Configuration (optional):** This command prevents git from tracking file permission changes.
   ```bash
   git config --global core.filemode false
   ```

