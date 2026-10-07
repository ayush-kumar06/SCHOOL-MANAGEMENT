# 🏫 SchoolOS – School Management System

SchoolOS is a simple **School Management System** built with Python. It provides a **Streamlit-based web interface** for managing students, teachers, and student grades.

The project also includes a **Python console-based implementation** demonstrating **Object-Oriented Programming (OOP)** concepts.

## ✨ Features

### 👨‍🎓 Student Management

- 📝 Register a new student
- 👤 Store student name, age, email, and roll number
- 🚫 Prevent duplicate roll numbers
- 📧 Validate email addresses
- 🔍 View complete student details
- 📊 View student grades and average score

### 👨‍🏫 Teacher Management

- 📝 Register a new teacher
- 👤 Store teacher name, age, email, subject, and employee ID
- 🚫 Prevent duplicate employee IDs
- 📧 Validate email addresses
- 🔍 View teacher details

### 📚 Grade Management

- 👨‍🎓 Select a registered student
- ➕ Add marks for different subjects
- 💯 Store marks between 0 and 100
- 📊 Automatically calculate student average
- 📋 Display subject-wise grades

### 📊 Dashboard

The Streamlit dashboard displays:

- 👨‍🎓 Total number of students
- 👨‍🏫 Total number of teachers
- 📝 Total grades recorded
- 📈 School average
- 👥 Recent students
- 🧑‍🏫 Faculty/teacher information

### 💾 Data Persistence

All records are stored in a local JSON file:

`school_data.json`

The application loads existing data when it starts and saves changes back to the JSON file.

## 📁 Project Structure

```text
SchoolOS/
│
├── app.py
├── main.py
├── school_data.json
├── demo.png
└── README.md
📋 File Description
File	Purpose
app.py	Streamlit web application and user interface
main.py	Console-based Python implementation using OOP
school_data.json	Local JSON database containing students, teachers, and grades
demo.png	Screenshot/demo of the SchoolOS dashboard
README.md	Project documentation
🛠️ Technologies Used
🐍 Python
🌐 Streamlit
🗃️ JSON
🧩 Object-Oriented Programming (OOP)
🎨 HTML/CSS for custom Streamlit UI styling
🧩 OOP Concepts Used

The project demonstrates several OOP concepts through the console implementation.

1️⃣ Abstract Class

Persons is an abstract base class containing common methods for students and teachers.

class Persons(ABC):

It defines abstract methods such as:

get_roles()
register()
show_details()
2️⃣ Inheritance

Student and Teacher inherit from the Persons class.

class Student(Persons):
class Teacher(Persons):
3️⃣ Abstraction

Common operations are defined in the parent class while student- and teacher-specific implementations are provided in their respective classes.

4️⃣ Static Method

Email validation is implemented as a static method:

@staticmethod
def validate_email(email):
5️⃣ Structured Data

Student and teacher information is maintained in structured dictionaries and stored in the JSON database.

🌐 Streamlit Application

The main web application is built using Streamlit.

The application contains the following navigation options:

🏠 Dashboard
👨‍🎓 Register Student
👨‍🏫 Register Teacher
📚 Add Grade
🔍 Student Details
🔍 Teacher Details
📊 Dashboard

The dashboard provides an overview of the school data.

It displays:

👨‍🎓 Total students
👨‍🏫 Total teachers
📝 Total grades recorded
📈 School average
👥 Recent students
🧑‍🏫 Faculty information

The school average is calculated from all recorded student grades.

👨‍🎓 Student Registration

The student registration form collects:

👤 Full Name
📧 Email Address
🎂 Age
🔢 Roll Number

The application checks that all required fields are filled, validates the email address, and prevents duplicate roll numbers before saving the student.

👨‍🏫 Teacher Registration

The teacher registration form collects:

👤 Full Name
📧 Email Address
📚 Subject
🎂 Age
🆔 Employee ID

The application validates the email address and prevents duplicate employee IDs.

📚 Add Grade

Grades can be added for registered students by entering:

👨‍🎓 Student
📖 Subject
💯 Marks

Marks are accepted from 0 to 100.

The grade is saved against the selected student and can later be viewed in the Student Details section.

🔍 Student Details

The Student Details section allows the user to select a student and view:

👤 Full Name
🔢 Roll Number
🎂 Age
📧 Email
📊 Average Score
📚 Subject-wise Grades

The average score is automatically calculated from the student's recorded grades.

🔍 Teacher Details

The Teacher Details section displays:

👤 Full Name
🆔 Employee ID
🎂 Age
📚 Subject
📧 Email

for the selected teacher.

💾 Data Storage

SchoolOS uses a JSON file as a lightweight local database.

school_data.json

The application loads existing data when it starts and saves new or updated information back to the JSON file.

The same JSON file is used by both the Streamlit application and the console-based implementation.

💻 Console Version

main.py provides a command-line version of the SchoolOS system.

The console menu supports:

1️⃣ Register a student
2️⃣ Register a teacher
3️⃣ Add grades
4️⃣ Show student details
5️⃣ Show teacher details

This version demonstrates the use of Object-Oriented Programming concepts such as:

🧩 Abstract classes
🔗 Inheritance
⚙️ Methods
🔧 Static methods
📦 Structured data handling
🚀 Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/SchoolOS.git
cd SchoolOS

Replace your-username/SchoolOS with your actual GitHub repository URL.

2️⃣ Install Dependencies

Make sure Python is installed on your system.

Install Streamlit using:

pip install streamlit
▶️ Run the Web Application

Run the following command:

python -m streamlit run app.py

After running the command, Streamlit will provide a local URL in the terminal.

Usually:

http://localhost:8501

Open the URL in your browser to use SchoolOS.

💻 Run the Console Version

To run the OOP-based console application:

python main.py

Then select an option from the displayed menu.

🔄 How the Application Works
                 🏫 SchoolOS
                     │
          ┌──────────┴──────────┐
          │                     │
     🌐 Streamlit           💻 Console
       Web App                main.py
          │                     │
          └──────────┬──────────┘
                     │
              🗃️ school_data.json
🔁 Basic Workflow
▶️ Start
   ↓
📂 Load school_data.json
   ↓
🏫 Open SchoolOS
   ↓
🧭 Choose an operation
   ↓
👨‍🎓 Register Student / 👨‍🏫 Teacher
   ↓
📚 Add Student Grades
   ↓
🔍 View Details
   ↓
📊 Dashboard Updates
   ↓
💾 Save Data to JSON
✅ Validation

The project includes basic validation:

⚠️ Required fields cannot be empty
📧 Email must contain @ and .
🔢 Student roll numbers must be unique
🆔 Teacher employee IDs must be unique
🎂 Student age is limited to 5–30 in the web interface
🎂 Teacher age is limited to 21–70 in the web interface
💯 Marks are limited to 0–100
🎨 User Interface

SchoolOS uses custom CSS to create a clean management-dashboard style interface with:

🌑 Dark sidebar
✍️ Custom typography
📊 Statistics cards
👨‍🎓 Student and teacher cards
📝 Form styling
🏷️ Grade indicators
✅ Success/error messages
📱 Responsive column-based layout
🗃️ Example Data

The application stores student and teacher information in school_data.json.

Example structure:

{
    "students": [
        {
            "name": "Student Name",
            "age": 19,
            "email": "student@example.com",
            "roll_no": "101",
            "grades": {
                "Math": 75
            }
        }
    ],
    "teachers": [
        {
            "name": "Teacher Name",
            "age": 35,
            "email": "teacher@example.com",
            "subject": "Computer",
            "emp_id": "1"
        }
    ]
}
⚠️ Important Note

school_data.json is used as a local JSON database for this project.

For a production-level school management system, a proper database such as MySQL, PostgreSQL, or MongoDB would be more suitable.

🔮 Future Improvements

Possible improvements for future versions:

🔐 Admin login and authentication
📅 Student attendance management
🔎 Search and filter functionality
✏️ Edit and delete records
🏫 Class and section management
📊 Attendance reports
📄 PDF report generation
🗄️ Database integration
👥 Role-based access control
🕐 Teacher timetable management
📈 Student performance charts
☁️ Cloud deployment
💾 Backup and restore functionality
🎓 Learning Outcomes

Through this project, the following concepts can be practiced:

🐍 Python programming
🌐 Streamlit application development
🗃️ JSON file handling
🔄 CRUD-style data management
🧩 Object-Oriented Programming
📦 Abstract classes
🔗 Inheritance
⚙️ Static methods
✅ Form validation
🎨 Dynamic UI design
💾 Data persistence
🔗 Git and GitHub project management
📌 Project Status

🟢 Status: Completed / Functional

The current version provides:

👨‍🎓 Student registration
👨‍🏫 Teacher registration
📚 Grade management
📊 Dashboard statistics
🔍 Student details
🔍 Teacher details
💾 JSON-based data persistence
👨‍💻 Author

Ayush Kumar

🎓 B.Tech CSE (AI & ML)

📜 License

This project is created for learning and educational purposes.
