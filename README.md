# 🐋 Wordpress Docker Enviroment
 


Replace `new-folder-name` with your desired folder name. This will not affect the functionality of the Docker setup or the WordPress environment.

## Docker Compose Tutorial 📚

This section will guide you on how to use Docker Compose for setting up a WordPress environment.

### ✅ Prerequisites 
- Ensure you have Docker and Docker Compose installed on your machine.

### 1. 🛠️ Clone the Repository 
If you haven't already, clone the repository:
```bash
git clone https://github.com/Zagaz/Wordpress-Docker-Enviroment.git
cd wordpress-docker-enviroment
```
#### 🗂️ Changing the Folder Name After Cloning 

After cloning the repository, you can change the folder name to suit your preferences. Simply navigate to the parent directory and rename the folder using the following command:

```bash
mv wordpress-docker-enviroment new-folder-name
```

### 2. ⚙️ Configuration 
- Open the `docker-compose.yaml` file to configure your services. You can specify the WordPress version, database settings, and other configurations.


### 3. 🚀 Starting the Services 
- To start your WordPress environment, run:
```bash
docker-compose up -d
```
This command will start the containers in detached mode.
- To stop your WordPress enviroment, run:
```bash
docker-compose down
```

### 4. 🌐 Accessing WordPress 
- Once the containers are running, you can access your WordPress site by navigating to `http://localhost:8000` in your web browser.

### 5. 🗃️ Accessing PHPMyAdmin
- - Once the containers are running, you can access your WordPress site by navigating to `http://localhost:8081` in your web browser.

### 6. 🛑 Stopping the Services ⏹️
- To stop the running services, use:
```bash
docker-compose down
```

### 7. 🗑️ Deleting the Environment
- To delete the Docker environment completely, you can run:
```bash
docker-compose down --volumes
```
This command will stop the containers and remove the associated volumes, effectively deleting the environment.

## 📄 Default .env Data 
[## 🐳 Default Docker Images and How to Change Them]

This environment uses Docker images for WordPress, the database, and phpMyAdmin. By default, these images are defined in the `docker-compose.yaml` file using environment variables from your `.env` file.

### Default Images

- **WordPress:** `${WORDPRESS_IMAGE}` (Default: `wordpress:latest`)
- **Database:** `${MYSQL_IMAGE}` (Default: `mariadb:latest`)
- **phpMyAdmin:** `${PHPMYADMIN_IMAGE}` (Default: `phpmyadmin/phpmyadmin:latest`)

### How to Change the Images

To use a different image or version, edit the corresponding variable in your `.env` file:

```env
WORDPRESS_IMAGE=wordpress:latest
MYSQL_IMAGE=mariadb:latest
PHPMYADMIN_IMAGE=phpmyadmin/phpmyadmin:latest
```

For example, to use MySQL instead of MariaDB, set:

```env
MYSQL_IMAGE=mysql:latest
```

After making changes, restart your containers:

```bash
docker compose down
docker compose up -d
```

This will apply your new image settings.

The default data in the `.env` file is provided to help you get started with your WordPress Docker environment. You can change these values as desired to suit your specific configuration needs.

**⚠️Important:** Be cautious when modifying the `.env` file, especially regarding sensitive data such as database credentials, API keys, and other private information. Ensure that sensitive data is kept secure and not exposed in public repositories or shared environments.

## 🎉 Conclusion 
You have successfully set up a WordPress environment using Docker Compose!


