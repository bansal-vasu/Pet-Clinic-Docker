# Project Title: Pet Clinic Dockerized Application

This project is based on the work of **feelgood1987** and **dsyer**, created in collaboration with the **Spring Boot Community** and hosted in the repository [spring-projects/spring-petclinic](https://github.com/spring-projects/spring-petclinic). Full credit goes to the original creators and contributors for their efforts in developing and maintaining this exemplary Spring Boot application.

I would also like to mention **ajeetraina** whose work, hosted in the repository [spring-petclinic-docker](https://github.com/dockersamples/spring-petclinic-docker?tab=readme-ov-file) helped me build a dockerized version of the original app. 

This project would not have been possible without the work of the original creators and all the contributors.

**INTRODUCTION**

This project involves creating a fully functional Pet Clinic application, packaged and deployed using Docker. The Pet Clinic application serves as a robust management tool for pet owners, veterinarians, and clinic administrators, enabling seamless operations and efficient management of pet-related information. The application is designed with user-friendly features that enhance the user experience, coupled with a dynamic in-memory database for data storage and retrieval.

**Application Features:**

 - **Add Pets:** Users can add pet profiles, including details such as name, species, and other attributes.
 - **Add Owners:** A feature to register and manage pet owner information.
- **Find Owners:** Search functionality to retrieve owner details efficiently.
- **Find Veterinarians:** Users can access a list of veterinarians registered in the system.
 - **Exception Handling:** Robust error-handling mechanisms ensure the system operates smoothly under various scenarios.
   
**Database Configuration:**

 - **In-Memory Database:** The application uses the H2 database in its default configuration, populated with sample data at startup.
 - **Database Console:** Accessible via http://localhost:8080/h2-console, allowing users to interact with the database directly.
 - **Dynamic Connection URL:** The database connection URL (jdbc:h2:mem:<uuid>) is generated at runtime and logged to the console for convenience.

**Docker Capabilities:**

 - **Isolation:** The application is containerized to ensure isolation from the host environment and other applications.
 - **Portability:** The Docker container allows the application to run consistently across various environments without compatibility issues.
 - **Ease of Deployment:** All dependencies, configurations, and runtime environments are packaged into a single Docker image for streamlined deployment.
 - **Scalability:** The Dockerized setup can be scaled horizontally, allowing multiple instances of the Pet Clinic to be deployed.
 - **Simplified Management:** Using Docker Compose or other orchestration tools, the application can be integrated with additional services or databases.

This project demonstrates the potential of combining Docker's capabilities with an interactive web application, showcasing expertise in both application development and containerization.

**Prerequisites:**

**Docker:** Make sure Docker is installed on your system. [Docker Installation Guide](https://docs.docker.com/get-docker/)  

**Steps to Set-Up this Docker:**

1. Open Ubuntu Terminal
   
2. Clone the github repository using the following command in the terminal:

   ```
   git clone https://github.com/dockersamples/spring-petclinic.git
   ```

4. After this run the following commands one after the other:

   ```
   cd spring-petclinic

   ./mvnw package

   java -jar target/*.jar
   ```

You can then access petclinic here: [http://localhost:8080/](http://localhost:8080/)

<img width="625" alt="petclinic" src="https://github.com/user-attachments/assets/73dcacbb-d4e1-449f-ba64-5d51392a3ba1">


**Note:** This is for the spring boot version of the application.

**To Create dockerized version:**

**Build a Container:**

```
 docker build -t petclinic-app . -f Dockerfile
```

 **Use Docker Compose**

 ```
  docker-compose up -d
```

  **DONE**
  
  You can then go to [http://localhost:8080/](http://localhost:8080/) to access this application.

**Conclusion**

The Pet Clinic application demonstrates the effective use of modern web application development practices, leveraging Spring Boot for a streamlined backend and Docker for deployment and scalability. It showcases how modular and maintainable code can be coupled with dynamic database management and robust exception handling to create a user-friendly and reliable system. This application serves as an excellent foundational tool for pet clinics to manage their operations efficiently, from maintaining pet records to tracking veterinarians and owners. In real-world scenarios, such systems can reduce administrative overhead, enhance service delivery, and improve customer satisfaction in pet care management.

**Recommendations**

To enhance the capabilities and utility of this application, the following improvements are suggested:

 - **Authentication and Authorization:** Implement role-based access control to ensure data privacy and secure access for administrators, veterinarians, and pet owners.

 - **Integration with External APIs:** Add integrations with APIs for scheduling (e.g., Google Calendar), payment gateways, or medical history databases to offer additional features like appointment scheduling and billing.

 - **Persistent Database Support:** Replace or extend the in-memory H2 database with a persistent database like PostgreSQL or MySQL to allow real-world deployment with data retention capabilities.

 - **Reporting and Analytics:** Include features to generate reports and analytics for clinic operations, such as veterinarian performance, popular pet breeds, and financial summaries.

 - **Cloud Deployment:** Deploy the application on cloud platforms like AWS or Azure for greater accessibility, scalability, and real-time monitoring.

 - **Multilingual Support:** Incorporate support for multiple languages to make the application more inclusive and accessible to users in diverse regions.

  

https://github.com/user-attachments/assets/6e60ee07-488d-4d14-ba9b-9682474b6a41



  **Reference(s):** [Building PetClinic app using Dockerfile](https://docs.docker.com/guides/java/containerize/)









