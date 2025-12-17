# Frequent Itemset Mining Dockerized App

#### Keywords

`Frequent Itemset Mining`, `Data Mining`, `Distributed Systems`, `Cloud Computing`, `Docker`, `Docker Compose`, `Apriori`, `FP-Growth`, `Flask`, `Python`, `Web Application`.

This project presents the design and implementation of a **distributed, containerized web application** for executing **frequent itemset mining algorithms** on user-provided datasets. The goal is to provide an accessible system that allows users to upload transactional data, select a mining algorithm, and receive the extracted frequent patterns asynchronously.

The application leverages **Docker** for containerization, enabling portability, scalability, and isolation of components. The backend executes **Apriori** and **FP-Growth** algorithms, while the frontend offers a simple web interface for dataset submission and request tracking. Results are delivered to the user via **email notification**, ensuring non-blocking execution of long-running tasks.

This project was developed as part of the coursework exam for the *Distributed Systems and Cloud Computing* course during the academic year **2022/2023**. 

---

### Key Features

* **Frequent Pattern Mining**: Extraction of frequent itemsets using Apriori and FP-Growth algorithms
* **Dockerized Architecture**: Full application containerization using Docker and Docker Compose
* **Asynchronous Processing**: Non-blocking execution with email-based result delivery
* **Web Interface**: HTML-based frontend for dataset upload and algorithm selection
* **Request Management**: Persistent storage of request history using a local database

---

### Project Structure

* **Web Interface**

  * HTML-based frontend built with Bootstrap
  * Allows users to upload `.csv` datasets, select the mining algorithm, and provide an email address
  * Includes a history page to track submitted requests and their status

* **Request Manager**

  * Backend logic implemented in Python using the **Flask** microframework
  * Handles HTTP requests, dataset validation, database interaction, and task orchestration

* **Frequent Mining Engine**

  * Implements **Apriori** and **FP-Growth** algorithms for pattern extraction
  * Uses Pandas and NumPy for dataset preprocessing and transformation

* **Database Layer**

  * Local **SQLite** database used to store request metadata (dataset name, algorithm, email, status)
  * Ensures persistence across application restarts

* **Notification Service**

  * Email-based notification system implemented via SMTP
  * Sends either the mining results or error notifications to the user upon task completion

* **Docker Infrastructure**

  * `Dockerfile`: Defines the application image and runtime environment
  * `docker-compose.yml`: Orchestrates containers and networking configuration

---

### Technologies Used

* **Programming Language**: Python
* **Web Framework**: Flask
* **Data Analysis**: Pandas
* **Containerization**: Docker, Docker Compose
* **Database**: SQLite
* **Communication**: SMTP (email notifications)

---

### Report

* **Technical Report (Italian)**:

  * Overview of Docker technology and container-based virtualization
  * Formal description of Apriori and FP-Growth algorithms
  * Detailed explanation of application architecture and implementation choices
  * Screenshots and examples of user interaction and result delivery
