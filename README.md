# User Management API with Email Notification  

## Description  
This is a **Spring Boot API** that allows adding users to a database and automatically sends a default email to the respective user upon registration.  

## Features  
- Add users to the database  
- Automatically send an email upon user creation  
- Uses **Spring Boot, Java, and SMTP** for email handling  

## Tech Stack  
- **Backend:** Java, Spring Boot, Spring Data JPA  
- **Database:** MySQL / PostgreSQL / H2  
- **Email Service:** JavaMailSender (SMTP)  

## Installation  

### 1. Clone the Repository  
```sh
 git clone https://github.com/your-username/your-repo.git
  cd your-repo

**2. Configure the Application**
  Update src/main/resources/application.properties with your database and email settings:
   # Database Configuration  
     spring.datasource.url=jdbc:mysql://localhost:3306/your_database  
     spring.datasource.username=root  
     spring.datasource.password=yourpassword  
     spring.jpa.hibernate.ddl-auto=update  

   # Email Configuration  
      spring.mail.host=smtp.example.com  
      spring.mail.port=587  
      spring.mail.username=your-email@example.com  
      spring.mail.password=your-email-password  
      spring.mail.properties.mail.smtp.auth=true  
      spring.mail.properties.mail.smtp.starttls.enable=true


**3. Build and Run the Application**
    mvn clean install
    mvn spring-boot:run

API Endpoints
   Add a New User & Send Email
   Endpoint: POST /api/users
    Request Body:
        {
          "name": "John Doe",
           "email": "johndoe@example.com"
        }

     Response:
        {
             "message Email sent succesfully"
        }

**Project Structure**

src  
│-- main  
│   ├── java/com/example/api  
│   │   ├── controller  
│   │   │   ├── UserController.java  
│   │   ├── entity  
│   │   │   ├── User.java  
│   │   ├── service  
│   │   │   ├── UserService.java  
│   │   │   ├── EmailService.java  
│   │   ├── ApiApplication.java  
│-- resources  
│   ├── application.properties
