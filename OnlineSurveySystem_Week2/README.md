# Online Survey System

A complete Online Survey System built with Spring Boot, Thymeleaf, and MySQL. This project allows users to create, share, and analyze surveys with a beautiful, modern user interface.

## Features

- **User Authentication**: Register, login, and logout with session management
- **Survey Creation**: Create detailed surveys with categories, expiry dates, visibility settings, and more
- **Survey Response**: Take surveys with rating scales, yes/no questions, and feedback fields
- **Results Viewing**: View survey results with average ratings and detailed responses
- **Public & Private Surveys**: Control survey visibility
- **Modern UI**: Custom color palette, gradients, animations, and responsive design

## Tech Stack

- **Java 17**
- **Spring Boot 3.1.5**
- **Spring Data JPA**
- **Thymeleaf**
- **MySQL**
- **Maven**

## Project Structure

```
src/main/java/com/example/survey/
├── controller/
│   ├── AuthController.java
│   ├── HomeController.java
│   └── SurveyController.java
├── service/
│   ├── UserService.java
│   └── SurveyService.java
├── repository/
│   ├── UserRepository.java
│   ├── SurveyRepository.java
│   └── ResponseRepository.java
└── entity/
    ├── User.java
    ├── Survey.java
    └── SurveyResponse.java

src/main/resources/
├── templates/
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── create-survey.html
│   ├── take-survey.html
│   ├── survey-results.html
│   ├── my-surveys.html
│   ├── public-surveys.html
│   └── thank-you.html
└── static/
    └── css/
        ├── theme.css
        └── animations.css
```

## Database Setup

1. Create MySQL database:
```sql
CREATE DATABASE online_survey_system;
```

2. Update `application.properties` with your MySQL credentials:
```properties
spring.datasource.username=root
spring.datasource.password=your_password
```

3. The application will automatically create tables using JPA (ddl-auto=update)

## Running the Application

1. Make sure MySQL is running
2. Update database credentials in `application.properties`
3. Build the project:
```bash
mvn clean install
```

4. Run the application:
```bash
mvn spring-boot:run
```

5. Open browser and navigate to:
```
http://localhost:8080
```

## Usage

1. **Register**: Create a new account
2. **Login**: Login with your credentials
3. **Create Survey**: Click "Create Survey" on dashboard to create a new survey
4. **My Surveys**: View all surveys you've created
5. **Public Surveys**: Browse and take public surveys
6. **View Results**: View responses and statistics for your surveys

## Features Details

### Survey Creation
- Title and description
- Category selection
- Purpose and target audience
- Expiry date
- Visibility (public/private)
- Survey tone (formal/casual/neutral)
- Estimated completion time
- Optional instructions

### Survey Response
- Overall satisfaction rating (1-5)
- Multiple Likert-scale questions
- Yes/No questions
- Open feedback textarea
- Optional suggestions field

### Results Viewing
- List of all responses
- Average rating calculation
- Detailed response table
- Submission timestamps

## UI Features

- Custom color palette (Deep Purple + Teal gradient)
- Smooth animations and transitions
- Card-based layout
- Responsive design
- Hover effects and visual feedback

## Notes

- Authentication uses HttpSession (no Spring Security)
- Passwords are stored as plain text (for demo purposes only)
- Database tables are auto-created on first run

## License

This project is created for educational purposes.