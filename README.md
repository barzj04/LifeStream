# 💖 LifeStream

Welcome to **LifeStream**! 🌊💡 This project is designed to streamline the management of blood donation and transfusion processes, ensuring efficient and effective communication between donors, medical institutions, and recipients.

## 📚 Table of Contents
- [🌟 Overview](#-overview)
- [🚀 Features](#-features)
- [🛠️ Technologies Used](#-technologies-used)
- [📥 Installation & Usage](#-installation--usage)
- [🗄️ Database Setup](#-database-setup)
- [📂 Project Structure](#-project-structure)
- [👥 Team Members](#-team-members)
- [🎓 University Information](#-university-information)
- [📜 License](#-license)
- [📧 Contact](#-contact)

## 🌟 Overview
LifeStream is a **blood donation management system** that connects **donors, hospitals, and blood banks** efficiently. 🏥💉 It allows real-time tracking of blood inventory, donation scheduling, and recipient needs to ensure that life-saving resources are available when needed.

## 🚀 Features
1. 🩸 **Donor Registration & Management** – Track and manage donor information.
2. 📊 **Blood Inventory Monitoring** – Keep real-time records of blood availability.
3. 🏥 **Hospital & Blood Bank Integration** – Seamless interaction between medical institutions.
4. 📅 **Appointment Scheduling** – Simplifies the process of booking donation appointments.
5. 🔔 **Notification System** – Alerts for low stock, urgent donations, and scheduled appointments.

## 🛠️ Technologies Used
- ☕ **Java** – Core backend development.
- 🗄️ **MySQL** – Database management.
- 🔗 **JDBC** – Java Database Connectivity for MySQL.
- 🌐 **Spring Boot** – Framework for backend services.
- 🎨 **Swing / JavaFX** – GUI development.

## 📥 Installation & Usage
### 🔧 Prerequisites
Ensure you have the following installed:
- ✅ Java Development Kit (JDK) 8 or higher
- ✅ MySQL for database management
- ✅ Git (optional, for cloning the repository)

### 📌 Installation Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/barzj04/LifeStream.git
   ```
2. Navigate to the project directory:
   ```sh
   cd LifeStream
   ```
3. Compile the Java files:
   ```sh
   javac -d bin src/com/mycompany/lifestream/*.java
   ```
4. Run the application:
   ```sh
   java -cp bin com.mycompany.lifestream.Main
   ```

## 🗄️ Database Setup
1. **Start MySQL Server**
   Ensure your MySQL server is running.
   ```sh
   mysql -u root -p
   ```
2. **Create the Database**
   ```sql
   CREATE DATABASE LifeStreamDB;
   ```
3. **Use the Database**
   ```sql
   USE LifeStreamDB;
   ```
4. **Create the `donor` Table**
   ```sql
   CREATE TABLE donor (
       donorId INT PRIMARY KEY AUTO_INCREMENT,
       fullName VARCHAR(100),
       fatherName VARCHAR(100),
       motherName VARCHAR(100),
       dateOfBirth DATE,
       mobileNumber VARCHAR(15),
       gender VARCHAR(10),
       email VARCHAR(100),
       bloodGroup VARCHAR(5),
       city VARCHAR(100),
       address TEXT
   );
   ```
5. **Configure Connection in `ConnectionProvider.java`**
   Update database credentials in the `ConnectionProvider.java` file:
   ```java
   public class ConnectionProvider {
       public static Connection getCon() {
           try {
               Class.forName("com.mysql.cj.jdbc.Driver");
               Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/LifeStreamDB", "root", "yourpassword");
               return con;
           } catch (Exception e) {
               System.out.println(e);
               return null;
           }
       }
   }
   ```
6. **Restart the Application**
   Now you can run the project, and it will connect to MySQL.

## 📂 Project Structure
```
LifeStream/
│── src/
│   ├── Main.java  # 🎬 Entry point of the application
│   ├── Donor.java  # 🩸 Manages donor details
│   ├── BloodInventory.java  # 🏥 Tracks blood stock levels
│   ├── Hospital.java  # 🏨 Handles hospital records
│   ├── Appointment.java  # 📅 Manages donation schedules
│   ├── DatabaseHandler.java  # 🗄️ Handles database operations
│── README.md  # 📖 Project documentation
│── LICENSE  # 📜 License information
```

## 👥 Team Members
- **Mohamad Akram bin Mohd Faisal**  
  - Matric ID: 22006626  
  - GitHub: [Akram Faisal](https://github.com/AkramFaisal)  
- **Arleen April Chong**  
  - Matric ID: 22006582  
  - GitHub: [Arleen 🦄](https://github.com/Arleen)  

## 🎓 University Information
- **University:** Universiti Teknologi PETRONAS  
- **Program:** Bachelor of Computer Science (Hons)  
- **Year/Semester:** 1st Year, 2nd Semester (January 2024)  
- **Course:** TFB1033: Object-Oriented Programming  
- **Instructor:** Dr. Arafat M. Rashad AlDhaqm 🧑‍🏫  

## 📜 License
This project is licensed under the MIT License. Check the [LICENSE](LICENSE) file for details.

## 📧 Contact
For any inquiries or suggestions, feel free to reach out or create an issue in the repository. We appreciate your feedback! 😊

---
💖 *Saving lives, one donation at a time!* 🩸✨

