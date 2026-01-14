# Rent a Car - Car Rental Service Application

A full-stack web application for managing a rent-a-car service using Spring Boot (backend) and Angular (frontend). This project features car booking, availability tracking, customer management, and rental history. Optimized for efficiency and user experience.

## 🚀 Features

- **User Authentication & Authorization**
  - User registration and login
  - Role-based access control (Admin and Customer)
  - JWT-based secure authentication

- **Car Management**
  - Add, update, and delete cars
  - Search and filter available cars
  - Car availability tracking
  - Image upload support

- **Booking System**
  - Book cars with date selection
  - View booking history
  - Admin booking management
  - Customer booking tracking

- **Dashboard**
  - Admin dashboard for managing cars and bookings
  - Customer dashboard for viewing bookings and searching cars

## 🛠️ Tech Stack

### Backend
- **Spring Boot** - Java framework for building REST APIs
- **Java 17** - Programming language
- **Maven** - Dependency management
- **JWT** - JSON Web Tokens for authentication
- **Spring Security** - Security framework

### Frontend
- **Angular 16** - Modern web framework
- **TypeScript** - Type-safe JavaScript
- **NG-Zorro** - Enterprise Angular UI component library
- **SCSS/Less** - CSS preprocessors

## 📋 Prerequisites

Make sure you have the following tools installed before setting up the application:

- **Node.js** - v12 or higher ([Download Node.js](https://nodejs.org/))
- **Angular CLI** - Install globally:
  ```bash
  npm install -g @angular/cli
  ```
- **Java Development Kit (JDK)** - Version 17 ([Download JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html))
- **Maven** - Build tool ([Download Maven](https://maven.apache.org/))
- **Database** - MySQL or compatible database

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/declared-as-ala/car_rental_spring_Angular.git
cd Angular-and-Spring-project
```

### 2. Database Configuration

1. Create a new database using the provided SQL file:
   ```bash
   # Import the database schema
   mysql -u your_username -p < rentacar_db.sql
   ```

2. Configure database connection in `Car-Rental-Service-Spring-Angular-NGZorro/Spring Boot/src/main/resources/application.properties`:
   ```properties
   spring.datasource.username=your_db_username
   spring.datasource.password=your_db_password
   spring.datasource.url=jdbc:mysql://localhost:3306/rentacar_db
   ```
   
   > **Note:** Update the username, password, and database URL according to your database configuration.

### 3. Backend Setup

1. Navigate to the Spring Boot project directory:
   ```bash
   cd Car-Rental-Service-Spring-Angular-NGZorro/Spring Boot
   ```

2. Build and run the Spring Boot application:
   ```bash
   # Using Maven wrapper
   ./mvnw spring-boot:run
   
   # Or using Maven directly
   mvn spring-boot:run
   ```
   
   The backend API will be available at `http://localhost:8080` (or the port configured in application.properties)

### 4. Frontend Setup

1. Navigate to the Angular project directory:
   ```bash
   cd Car-Rental-Service-Spring-Angular-NGZorro/Angular
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the Angular development server:
   ```bash
   ng serve
   ```
   
   The frontend application will be available at `http://localhost:4200`

4. Build for Production:
   ```bash
   ng build --prod
   ```

## 🎯 Usage

### Access the Application

- Open your browser and navigate to `http://localhost:4200`

### Default Login Credentials

**Admin Account:**
- Email: `admin@test.com`
- Password: `admin`

**Customer Account:**
- Email: `yuwantha@gmail.com`
- Password: `12345`

### Getting Started

1. **As Admin:**
   - Login with admin credentials
   - Access admin dashboard
   - Add, update, or delete cars
   - View and manage all bookings

2. **As Customer:**
   - Register a new account or login
   - Search for available cars
   - Book a car by selecting dates
   - View your booking history

## 📁 Project Structure

```
Angular-and-Spring-project/
├── Car-Rental-Service-Spring-Angular-NGZorro/
│   ├── Angular/                    # Angular frontend application
│   │   ├── src/
│   │   │   ├── app/
│   │   │   │   ├── auth/          # Authentication components
│   │   │   │   ├── modules/
│   │   │   │   │   ├── admin/     # Admin module
│   │   │   │   │   └── customer/  # Customer module
│   │   │   │   └── services/      # Angular services
│   │   │   └── assets/            # Static assets
│   │   └── package.json
│   └── Spring Boot/               # Spring Boot backend
│       ├── src/
│       │   └── main/
│       │       ├── java/
│       │       │   └── com/coderdot/
│       │       │       ├── controllers/    # REST controllers
│       │       │       ├── services/       # Business logic
│       │       │       ├── repositories/   # Data access layer
│       │       │       ├── entities/       # Entity models
│       │       │       ├── dtos/           # Data transfer objects
│       │       │       └── configurations/ # Security config
│       │       └── resources/
│       │           └── application.properties
│       └── pom.xml
├── rentacar_db.sql                 # Database schema
└── README.md
```

## 🔐 Security Features

- JWT token-based authentication
- Role-based access control (Admin/Customer)
- Spring Security integration
- CORS configuration for cross-origin requests
- Password encryption

## 📝 API Endpoints

The application provides RESTful APIs for:
- Authentication (login, signup)
- Car management (CRUD operations)
- Booking management
- User management
- Search functionality

## 🐛 Troubleshooting

- **Database Connection Issues:** Ensure your database is running and credentials in `application.properties` are correct
- **Port Conflicts:** Check if ports 8080 (backend) and 4200 (frontend) are available
- **Dependencies:** Run `npm install` in the Angular directory if you encounter module errors
- **Build Errors:** Ensure JDK 17 is installed and Maven is properly configured

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 About the Author

**Ala Missaoui**

- 📧 Email: [alamissaoui.dev@gmail.com](mailto:alamissaoui.dev@gmail.com)
- 🔗 GitHub: [@declared-as-ala](https://github.com/declared-as-ala)

This project was forked and enhanced to demonstrate full-stack development skills with Spring Boot and Angular, focusing on building a complete car rental management system with role-based access control and modern UI components.

## 🙏 Acknowledgments

- Original project by [yuwantha98](https://github.com/yuwantha98/Angular-and-Spring-project)
- Built with Spring Boot, Angular 16, and NG-Zorro UI components

---

**Note:** This project demonstrates a complete full-stack application with authentication, role-based access control, and modern web development practices. The application is optimized for efficiency and provides an excellent user experience for both administrators and customers.
