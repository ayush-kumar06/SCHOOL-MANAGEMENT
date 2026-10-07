🏫 SchoolOS – School Management System

A simple and interactive school management system built with Python, Streamlit, Object-Oriented Programming, and JSON-based data persistence.

✨ Features
👨‍🎓 Student Management
Register new students
Store student name, age, email, and roll number
Prevent duplicate roll numbers
Validate email addresses
View student details
View subject-wise grades
Calculate average marks
👨‍🏫 Teacher Management
Register teachers
Store teacher name, age, email, subject, and employee ID
Prevent duplicate employee IDs
Validate email addresses
View teacher details
📚 Grade Management
Select registered students
Add subject-wise marks
Validate marks between 0–100
Calculate student average
Display subject-wise performance
📊 Dashboard
Total students
Total teachers
Total recorded grades
Overall school average
Recent students
Faculty information
💾 Data Persistence
Stores data in a local JSON file
Automatically loads existing data when the application starts
Saves new students, teachers, and grades
Data remains available even after restarting the application
🖥️ Interactive Web Interface
Built using Streamlit
Sidebar navigation
Custom UI styling
Forms and validation
Success and error messages
Responsive layout
🧱 Object-Oriented Programming
Abstract classes
Inheritance
Abstraction
Static methods
Encapsulation of student and teacher operations
📌 Overview

SchoolOS is a Python-based School Management System designed to manage basic school information in a simple and organized way.

The application provides two interfaces:

🌐 Streamlit Web Application
💻 Python Console Application

The Streamlit application provides an interactive dashboard where users can register students, register teachers, add grades, and view academic information.

The console application demonstrates how the same management system can be implemented using Object-Oriented Programming concepts in Python.

The project uses a local school_data.json file for storing information, making the application persistent without requiring a separate database.

🎯 Project Objectives

The main objectives of SchoolOS are:

To create a simple school management system using Python.
To manage student and teacher information.
To store and manage student grades.
To calculate student and school-level averages.
To demonstrate Object-Oriented Programming concepts.
To implement data validation.
To provide data persistence using JSON.
To create an interactive web interface using Streamlit.
To understand how Python applications can be connected with a user interface.
🏗️ System Architecture
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
                 ▼                           ▼
        ┌─────────────────┐        ┌─────────────────┐
        │ Streamlit Web UI│        │ Console Program │
        │     app.py      │        │     main.py     │
        └────────┬────────┘        └────────┬────────┘
                 │                          │
                 └────────────┬─────────────┘
                              ▼
                    ┌──────────────────┐
                    │  Data Validation │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Application Data │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ school_data.json │
                    └──────────────────┘
👨‍🎓 Student Management

SchoolOS allows users to register and manage student information.

Student Registration

The registration form collects:

👤 Full Name
📧 Email Address
🎂 Age
🆔 Roll Number

Before registering a student, the system checks:

Required fields are not empty.
Email format is valid.
Roll number is unique.
Age is within the allowed range.
Student Information

Each student record contains:

Name
Age
Email
Roll Number
Grades
Average Marks

Students can later be selected while adding grades.

👨‍🏫 Teacher Management

SchoolOS also provides a separate teacher management system.

Teacher Registration

The teacher registration form contains:

👤 Full Name
📧 Email Address
📚 Subject
🎂 Age
🆔 Employee ID

The system validates the entered information before saving it.

Teacher Information

Each teacher record contains:

Name
Age
Email
Subject
Employee ID

Duplicate employee IDs are not allowed.

📚 Grade Management

SchoolOS provides a dedicated section for adding student grades.

The user can:

Select a registered student.
Enter the subject name.
Enter marks.
Validate marks.
Save the grade.

Marks are restricted to:

0 ≤ Marks ≤ 100

The system stores grades subject-wise.

Example
Student: Ayush Kumar

Python     : 90
AI         : 85
Mathematics: 80

The system can then calculate the student's average marks.

📊 Dashboard

The SchoolOS dashboard provides a quick overview of the school's data.

Dashboard Statistics
┌──────────────────┐
│ Total Students   │
├──────────────────┤
│ Total Teachers   │
├──────────────────┤
│ Total Grades     │
├──────────────────┤
│ School Average   │
└──────────────────┘

The dashboard also displays:

📌 Recently registered students
👨‍🏫 Teacher/faculty information
📈 Overall academic performance
📊 School statistics

The school average is calculated using the recorded student grades.

💾 Data Persistence

SchoolOS uses a lightweight JSON-based data persistence system to store student, teacher, and grade information.

All application data is stored locally in:

school_data.json

The application automatically loads existing data when it starts and saves updated data whenever a new student, teacher, or grade is added.

🔄 Data Flow
User Input
    ↓
Streamlit / Console Application
    ↓
Validate Data
    ↓
Update Application Data
    ↓
Save to school_data.json
    ↓
Data Persists After Application Restart
📄 Stored Data

The JSON file maintains information such as:

👨‍🎓 Student Data
Name
Age
Email
Roll Number
Subject-wise Grades
Average Score
👨‍🏫 Teacher Data
Name
Age
Email
Subject
Employee ID
🗂️ Example JSON Structure
{
  "students": [
    {
      "name": "Ayush Kumar",
      "age": 20,
      "email": "ayush@example.com",
      "roll_no": "101",
      "grades": {
        "Python": 90,
        "AI": 85
      }
    }
  ],
  "teachers": [
    {
      "name": "Rahul Sharma",
      "age": 35,
      "email": "rahul@example.com",
      "subject": "Python",
      "employee_id": "T101"
    }
  ]
}
🔁 Persistence Process
Application starts → existing data is loaded from school_data.json.
User registers a student or teacher → input is validated.
User adds a grade → marks are validated between 0–100.
Data is updated → new information is added to the existing records.
JSON file is saved → changes are permanently stored locally.
Application restarts → previously saved data is loaded again.

This allows SchoolOS to maintain data between different application sessions without requiring a separate database system.

Note: JSON is suitable for learning and local applications. A production-level system could use MySQL, PostgreSQL, MongoDB, or another database system.

🧱 Object-Oriented Programming

One of the main purposes of SchoolOS is to demonstrate important Object-Oriented Programming concepts in Python.

1. 🔹 Abstract Class

The project uses an abstract base class:

class Persons(ABC):

The class defines common methods that can be implemented by different types of people in the system.

Methods include:

get_roles()
register()
show_details()
2. 🔹 Inheritance

Student and Teacher classes inherit from the common Persons class.

             Persons
                │
        ┌───────┴───────┐
        │               │
     Student          Teacher

This reduces code duplication and allows common functionality to be shared.

3. 🔹 Abstraction

Abstraction is used to define common behavior without exposing unnecessary implementation details.

The abstract Persons class provides a common structure for students and teachers.

4. 🔹 Static Method

The project uses a static method for email validation:

validate_email(email)

This method can validate an email without requiring an object instance.

5. 🔹 Structured Data

Student and teacher information is organized using Python dictionaries and stored in JSON format.

This makes the data:

Easy to understand
Easy to update
Easy to save
Easy to load
🌐 Streamlit Web Application

The main web application is developed using Streamlit.

The sidebar provides navigation between different sections.

Navigation
🏠 Dashboard

👨‍🎓 Register Student

👨‍🏫 Register Teacher

📚 Add Grade

🎓 Student Details

👨‍🏫 Teacher Details

This makes the application easy to navigate and use.

📝 Student Registration Workflow
Open Register Student
        ↓
Enter Student Information
        ↓
Validate Required Fields
        ↓
Validate Email
        ↓
Check Duplicate Roll Number
        ↓
Register Student
        ↓
Save Data to JSON
        ↓
Display Success Message
📝 Teacher Registration Workflow
Open Register Teacher
        ↓
Enter Teacher Information
        ↓
Validate Required Fields
        ↓
Validate Email
        ↓
Check Duplicate Employee ID
        ↓
Register Teacher
        ↓
Save Data to JSON
        ↓
Display Success Message
📚 Grade Addition Workflow
Select Student
      ↓
Enter Subject
      ↓
Enter Marks
      ↓
Validate Marks (0–100)
      ↓
Add Grade
      ↓
Calculate Average
      ↓
Save Data
🎓 Student Details

The Student Details section displays information about a selected student.

It can show:

Student Name
Roll Number
Age
Email
Average Marks
Subject-wise Grades
Example
Student: Ayush Kumar
Roll No: 101
Age: 20
Email: ayush@example.com

Grades
----------------------
Python       90
AI           85
Mathematics  80
----------------------
Average      85.0
👨‍🏫 Teacher Details

The Teacher Details section displays information about registered teachers.

Example:

Teacher Name : Rahul Sharma
Employee ID  : T101
Age          : 35
Subject      : Python
Email        : rahul@example.com
🛡️ Data Validation

SchoolOS contains multiple validation checks to maintain clean and valid data.

Validation	Description
Required Fields	Prevents empty mandatory fields
Email Validation	Checks basic email format
Roll Number	Prevents duplicate student roll numbers
Employee ID	Prevents duplicate teacher IDs
Student Age	Validates student age
Teacher Age	Validates teacher age
Marks	Allows marks only from 0–100
Student Age

The web interface validates student age between:

5 – 30 years
Teacher Age

Teacher age is validated between:

21 – 70 years
Marks

Marks must be:

0 – 100
🎨 User Interface

The Streamlit application includes custom styling to provide a clean and modern interface.

UI Elements
🌑 Dark sidebar
✨ Custom typography
📊 Statistics cards
👨‍🎓 Student cards
👨‍🏫 Teacher cards
📝 Styled forms
📈 Grade indicators
✅ Success messages
❌ Error messages
📱 Responsive column layout
📸 Application Preview

Add your application screenshot here:

<p align="center">
  <img src="demo.png" width="900">
</p>
🛠️ Tech Stack
Technology	Purpose
🐍 Python	Core programming language
🎨 Streamlit	Web application and UI
🗂️ JSON	Local data storage
🧱 OOP	Application architecture
🔤 HTML/CSS	Custom UI styling
💻 Git	Version control
🐙 GitHub	Source code hosting
📊 Data Storage

The project uses a local JSON file instead of a traditional database.

school_data.json
Why JSON?

JSON was selected because it is:

Simple
Lightweight
Human-readable
Easy to modify
Easy to load using Python
Suitable for a small educational project

For a larger production system, the application can be migrated to a proper database.

📁 Project Structure
SchoolOS/
│
├── app.py
│   └── Streamlit web application
│
├── main.py
│   └── Console-based OOP implementation
│
├── school_data.json
│   └── Student, teacher and grade data
│
├── demo.png
│   └── Application screenshot
│
└── README.md
    └── Project documentation
💻 Console Application

Along with the Streamlit interface, SchoolOS also contains a console-based implementation in main.py.

The console application provides a menu-driven system.

Main Menu
1. Register a student
2. Register a teacher
3. Add grades
4. Show student details
5. Show teacher details

This implementation demonstrates how the application's functionality can be handled using Python classes and Object-Oriented Programming.

🚀 Installation & Setup
📋 Prerequisites

Make sure Python is installed on your system.

Check Python version:

python --version
1️⃣ Clone the Repository
git clone https://github.com/ayush-kumar06/SchoolOS.git

Move into the project directory:

cd SchoolOS
2️⃣ Install Dependencies

Install Streamlit:

pip install streamlit

If your project contains a requirements file, you can also use:

pip install -r requirements.txt
3️⃣ Run the Streamlit Application

Run:

python -m streamlit run app.py

The application will open in your browser.

▶️ Usage

After launching the application:

Step 1 — Open Dashboard

View:

Total students
Total teachers
Total grades
School average
Recent students
Faculty information
Step 2 — Register Student

Enter the required student information and register the student.

Step 3 — Register Teacher

Enter teacher information and create a teacher record.

Step 4 — Add Grade

Select a student and add marks for a particular subject.

Step 5 — View Details

Open Student Details or Teacher Details to view stored information.

Step 6 — Restart Application

Close and restart the application.

Previously saved information will still be available because the data is stored in:

school_data.json
🔄 Complete Application Workflow
                ┌──────────────┐
                │    Start     │
                └──────┬───────┘
                       ↓
             ┌───────────────────┐
             │ Load JSON Data    │
             └─────────┬─────────┘
                       ↓
             ┌───────────────────┐
             │     Dashboard     │
             └─────────┬─────────┘
                       ↓
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
   Register       Register        Add Grade
    Student        Teacher            │
        │              │              │
        └──────────────┼──────────────┘
                       ↓
                Validate Data
                       ↓
                 Update Records
                       ↓
              Save school_data.json
                       ↓
                View Information
🧠 Core Concepts Used

This project helped implement and understand several Python concepts:

Python
Variables
Functions
Lists
Dictionaries
Loops
Conditional statements
Exception handling
File handling
JSON handling
Object-Oriented Programming
Classes
Objects
Inheritance
Abstraction
Abstract classes
Static methods
Streamlit
Sidebar navigation
Forms
Buttons
Select boxes
Input fields
Columns
Metrics
Success/error messages
Custom HTML/CSS
Data Management
JSON serialization
JSON deserialization
Data validation
Persistent local storage
CRUD-style operations
📈 Future Improvements

The current version focuses on core school management functionality. The system can be extended with:

🔐 Admin login and authentication
👥 Role-based access control
📅 Student attendance management
🔎 Student and teacher search
🔍 Advanced filtering
✏️ Edit existing records
🗑️ Delete records
🏫 Class and section management
📊 Attendance reports
📄 PDF report generation
🗄️ MySQL/PostgreSQL database
👨‍🏫 Teacher timetable management
📈 Advanced performance charts
☁️ Cloud deployment
💾 Database backup and restore
📱 Improved mobile interface
🎓 Learning Outcomes

Through this project, I learned and practiced:

🐍 Python programming
🧱 Object-Oriented Programming
🔗 Inheritance and abstraction
📦 Working with JSON data
💾 Data persistence
🎨 Streamlit application development
📝 Form handling
🛡️ Input validation
📊 Data presentation
🔄 CRUD-style application logic
🌐 Building interactive web applications
🐙 Git and GitHub project management
📌 Project Status
✅ Project Completed
✅ Student Management
✅ Teacher Management
✅ Grade Management
✅ Dashboard
✅ JSON Data Persistence
✅ Data Validation
✅ Streamlit UI
✅ Console Application
👨‍💻 Author
Ayush Kumar

B.Tech CSE (AI & ML)

<p> <a href="https://github.com/ayush-kumar06">🐙 GitHub</a> &nbsp; | &nbsp; <a href="https://www.linkedin.com/in/ayush-kumar-161380327">💼 LinkedIn</a> </p>
🙏 Acknowledgements

This project was developed as a learning project to practice:

Python
Object-Oriented Programming
Streamlit
JSON data handling
Data validation
Web application development
Git and GitHub
⭐ Support

If you found this project useful or interesting, consider giving the repository a ⭐ on GitHub.

It helps support the project and encourages further development.

<p align="center">
🏫 SchoolOS

Simple • Interactive • Persistent • Python Powered

Made with ❤️ using Python & Streamlit

</p>
