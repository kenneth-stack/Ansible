
## Project Based Task: Automated Deployment and Configuration with Ansible for Boilerplates

 Your task is to set up a new instance of the  java  boilerplate using Infrastructure as Code (IaC) with Ansible. The setup should include the following:

**Clone and Deploy**:
 Clone the DevOps branch of your boilerplate repository to a Linux server.
 Deploy the boilerplate application on the server.

**Install Dependencies**:
 Install all dependencies required for your boilerplate to run, including databases and messaging queues.

**Setup PostgreSQL**:
 Configure a PostgreSQL database.
 Save the admin user and credentials in /var/secrets/pg_pw.txt.

**Messaging Queue**:
 Set up any required messaging queue (e.g., RabbitMQ, Redis).

**Application Configuration**:
 Ensure your application starts on port 3000.
 Set up Nginx to reverse proxy your application to port 80.

**Logging**:
 Configure stderr logs to be saved in /var/log/stage_5b/error.log and stdout logs in /var/log/stage_5b/out.log.
 Ensure both log files are owned by the hng user.

**Database and Dependencies**:
 Install PostgreSQL and save the admin credentials in /var/secrets/pg_pw.txt.

 Install all application dependencies, including databases and messaging queues, and configure the environment variables or application settings accordingly.

**Application and Proxy Setup**:
 Ensure the application is running on 127.0.0.1:3000 without exposing port 3000 externally.
 Install Nginx 1.26 and configure it to reverse proxy requests from port 80 to your application.

**Logging Configuration**:
 Set up logging so that stderr logs are written to /var/log/stage_5b/error.log and stdout logs to /var/log/stage_5b/out.log, with both files owned by the hng user.

 
## summary 

**Essential Packages Installation**:
   - Installs necessary packages including Git, Java (OpenJDK 17), Maven, PostgreSQL, and Nginx.

**PostgreSQL Configuration**:
   - Sets up a PostgreSQL database (`hng_db`) and user (`postgres`) with appropriate permissions.
   - Stores credentials securely and ensures the database is running.

**Application Build and Run**:
   - Uses Maven to build the Java application (`./mvnw clean install`).
   - Runs the application using the generated JAR file (`your-app.jar` should be replaced with the actual file name).

**Nginx Configuration**:
   - Configures Nginx to act as a reverse proxy for the application.

**Testing**:
   - Runs the tests included in the `src/test/java/hng_java_boilerplate` directory using Maven (`./mvnw test`).

