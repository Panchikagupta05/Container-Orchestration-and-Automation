🐬 Setting Up MySQL in a Docker Container with an Initialization Script 🚀
📌 Prerequisites
✅ Install Docker on your system.
✅ Ensure Docker is running.
✅ Create an SQL initialization script (e.g., Panchika_demo.sql) with database and table definitions.
📂 Project Directory Structure
Ensure your project directory is organized as follows:

project-directory/
│── Dockerfile
│── Panchika_demo.sql
This structure keeps all necessary files in one place for an efficient setup.

🛠 Step 1: Create a Dockerfile
Create a Dockerfile in your project directory:

# 🏗 Use the official MySQL image
FROM mysql:latest

# 📂 Copy initialization script to the container
COPY Panchika_demo.sql /docker-entrypoint-initdb.d/

# 🔥 Expose MySQL port
EXPOSE 3306
📜 Step 2: Create an SQL Initialization Script
Create a file named Panchika_demo.sql in the same directory:

CREATE DATABASE Panchika;
USE Panchika;

CREATE TABLE students (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT
);

INSERT INTO students (name, age) VALUES ('Alice', 22), ('Bob', 24);
🏗 Step 3: Build the Docker Image
Run the following command to build the Docker image:

docker build -t mysql-custom .
💡 This command creates a custom MySQL image named mysql-custom.

🚀 Step 4: Run MySQL Container
To start a MySQL container using the custom image and set the root password, execute:

docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -d mysql-custom
🧐 Explanation:
🏷 Creates a container named mysql-container.
🔐 Sets the root password to root.
🏃 Runs the container in detached mode (-d).
🛠 Uses the custom MySQL image mysql-custom.
🔍 Step 5: Access the Running Container
To enter the running container’s shell:

docker exec -it mysql-container bash
💡 This command opens an interactive terminal session inside mysql-container.

💻 Step 6: Connect to MySQL
Once inside the container, access MySQL using:

mysql -u root -p
🔑 Enter the root password (root) when prompted.

🏗 Step 7: Verify Database and Tables
After logging into MySQL, check the available databases:

SHOW DATABASES;
🔄 Switch to the Panchika database:

USE Panchika;
📊 Query the students table:

SELECT * FROM students;
🎉 Conclusion
🎯 You have successfully set up MySQL in a Docker container with an initialization script. This method ensures that the database is automatically initialized with predefined schemas and data when the container starts. 🚀 Happy coding! 🎨