# 🏫 SchoolOS — School Management System

A school management system built in Python 🐍 to practice **Object-Oriented Programming (OOP)**. It lets you register students and teachers, record grades, and view details. It comes in two flavors:

- 🌐 **Web app** (`app.py`): a Streamlit interface with a dashboard and a custom UI.
- 💻 **Command-line app** (`main.py`): a menu-driven terminal version built with OOP (abstract classes and inheritance).

Both versions share the same JSON file (`school_data.json`) as their database 🗄️.

## 📸 Screenshot

![SchoolOS Dashboard](demo.png)

## ✨ Features

- 📊 Dashboard with totals: students, teachers, grades recorded, and school-wide average
- 🎓 Register students (name, age, email, roll number)
- 👨‍🏫 Register teachers (name, age, email, subject, employee ID)
- 📝 Add or update a student's grade for any subject
- 🔍 View student details with per-subject marks and average
- 🧑‍💼 View teacher details
- ✅ Email validation and duplicate checks (roll number / employee ID)
- 💾 Persistent storage in a JSON file

## 🧠 OOP Concepts Used (main.py)

| Concept | Where it is used |
|---------|------------------|
| 🎭 **Abstraction** | `Persons` is an abstract base class (`ABC`) with abstract methods `get_roles`, `register`, `show_details` |
| 🧬 **Inheritance** | `Student` and `Teacher` extend `Persons` |
| 🔄 **Polymorphism** | Each subclass implements its own `register` and `show_details` |
| 🔧 **Static method** | `Persons.validate_email` is shared by all subclasses |

## 📁 Project Structure

```
.
├── app.py              # 🌐 Streamlit web app (SchoolOS UI)
├── main.py             # 💻 Command-line version (OOP with ABC)
├── school_data.json    # 🗄️ JSON "database" (auto-updated)
├── demo.png            # 📸 Dashboard preview
└── README.md           # 📖 You are here
```

## 📋 Requirements

- 🐍 Python 3.8+
- 🎈 Streamlit (only for the web app)

## 🛠️ Installation

```bash
pip install streamlit
```

## 🚀 Usage

### 🌐 Web app (recommended)

```bash
streamlit run app.py
```

Then open the URL shown in the terminal (usually http://localhost:8501).

Sidebar pages:

| Page                 | What it does                                  |
|----------------------|-----------------------------------------------|
| 📊 Dashboard         | Overview stats, recent students, faculty list |
| 🎓 Register Student  | Add a new student                             |
| 👨‍🏫 Register Teacher  | Add a new teacher                             |
| 📝 Add Grade         | Save marks for a student's subject            |
| 🔍 Student Details   | View a student's profile and grades           |
| 🧑‍💼 Teacher Details   | View a teacher's profile                      |

### 💻 Command-line app

```bash
python main.py
```

Choose an option:

```
1  🎓 register a student
2  👨‍🏫 register a teacher
3  📝 add grades
4  🔍 show a student detail
5  🧑‍💼 show a teacher detail
```

## 🗃️ Data Format

`school_data.json` is created/updated automatically:

```json
{
    "students": [
        {
            "name": "Ankit Kumar",
            "age": 18,
            "email": "ankit@gmail.com",
            "roll_no": "226",
            "grades": { "English": 61.0 }
        }
    ],
    "teachers": [
        {
            "name": "Ashish Singh",
            "age": 35,
            "email": "ashish@gmail.com",
            "subject": "computer",
            "emp_id": "2"
        }
    ]
}
```

## 🧰 Tech Stack

- 🐍 Python
- 🎈 Streamlit
- 📄 JSON file storage
- 🎨 Custom CSS (Syne and DM Sans fonts)

## 👤 Author

**Ayush Kumar**
🎓 Department of AI & ML

- 🐙 GitHub: [ayush-kumar06](https://github.com/ayush-kumar06)
- 💼 LinkedIn: [Ayush Kumar](https://www.linkedin.com/in/ayush-kumar-161380327)

Built as a learning project for Python OOP concepts and Streamlit 💡
