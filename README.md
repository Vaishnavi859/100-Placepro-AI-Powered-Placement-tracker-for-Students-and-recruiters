# 🎓 Placement Prediction & Management System

A full-stack **Placement Prediction & Management System** built using **Python, Django, SQLite, and Machine Learning**. The system helps students manage placement activities, allows HR teams to search and evaluate candidates, and provides placement officers with complete administrative control.

The project also integrates a **Random Forest Classifier** to predict a student's placement probability based on academic performance, employability test scores, work experience, and other profile features.

---

## 🚀 Project Overview

The Placement Prediction & Management System provides a centralized platform for managing the complete campus placement process.

### 👨‍🎓 Students can:

* Register and securely log in
* Manage their profile
* Upload resumes
* Add and manage certifications
* Search placement drives
* Apply for suitable job opportunities
* Get ML-based placement predictions
* View placement probability and expected salary range
* Receive personalized improvement suggestions

### 👔 HR can:

* Log in to the system
* View placement drives
* View students who applied for drives
* Search and filter students
* View candidate profiles
* Download student resumes

### 👨‍💼 Placement Officers can:

* Manage HR accounts
* Create and manage placement drives
* View registered students
* Manage applications
* View placement statistics
* Access ML model visualizations
* Manage the overall placement process

---

## 🤖 Machine Learning

The project uses a **Random Forest Classifier** for placement prediction.

### Model Details

| Component                 | Details                  |
| ------------------------- | ------------------------ |
| Algorithm                 | Random Forest Classifier |
| Problem Type              | Binary Classification    |
| Dataset                   | 50 historical records    |
| Input Features            | 12                       |
| Output                    | Placed / Not Placed      |
| Training Accuracy         | 92%                      |
| Testing Accuracy          | 90%                      |
| Cross-Validation Accuracy | 88%                      |
| Precision                 | 89%                      |
| Recall                    | 87%                      |
| F1-Score                  | 88%                      |

The project documentation reports approximately **90% testing accuracy** for the model.

### 📊 Input Features

The model uses:

1. Gender
2. SSC Percentage
3. SSC Board
4. HSC Percentage
5. HSC Board
6. HSC Stream
7. Degree Percentage
8. Degree Type
9. Work Experience
10. Employability Test Percentage
11. MBA Specialization
12. MBA Percentage

The prediction provides:

* Placement prediction
* Placement probability
* Expected salary range
* Personalized improvement suggestions

---

## 📈 ML Visualizations

The application provides multiple visualizations to understand model performance:

* 📊 Model Accuracy Plot
* 🔍 Feature Importance Chart
* 🎯 Confusion Matrix
* 📈 Training & Validation Accuracy
* 📋 Dataset Distribution
* 📊 Performance Metrics

These visualizations are available through the **ML Visualizations** section of the application.

---

## 🛠️ Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript
* Font Awesome
* Responsive UI

### Backend

* Python
* Django 5.2.7

### Database

* SQLite

### Machine Learning

* Scikit-learn
* Pandas
* NumPy
* Random Forest Classifier

### Data Visualization

* Matplotlib
* Seaborn

### Other Tools

* Joblib
* Pillow

The project uses Django 5.2.7 and Python 3.8+.

---

## ✨ Key Features

### 🔐 Authentication

* Student login & registration
* HR login
* Placement Officer login
* Password-based authentication
* Session management

### 🎓 Student Module

* Student registration
* Profile management
* Resume upload
* Certification management
* Placement-drive search
* Job application
* Placement prediction
* Personalized recommendations

### 🏢 HR Module

* Candidate search
* Application management
* Student filtering
* Student profile viewing
* Resume downloading

### 👨‍💼 Placement Officer Module

* HR management
* Placement-drive management
* Student management
* Application monitoring
* Dashboard statistics
* ML visualization access

### 🎨 UI/UX

* Responsive design
* Modern gradient-based interface
* Background images
* Interactive cards
* Form validation
* Tooltips
* Responsive tables
* Mobile-friendly navigation

---

## 🗂️ Project Architecture

```text
placement_prediction_project/
│
├── mainapp/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── utils.py
│   ├── admin.py
│   └── migrations/
│
├── placement_prediction_project/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── static/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── main.js
│   ├── images/
│   └── plots/
│
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── student_*.html
│   ├── hr_*.html
│   ├── placement_officer_*.html
│   └── model_visualizations.html
│
├── resume_templates/
├── media/
│   ├── resumes/
│   └── certificates/
│
├── db.sqlite3
├── manage.py
└── README.md
```

The project structure and major application components are documented in the supplied project summary.

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/placement-prediction-system.git

cd placement-prediction-system
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**Linux / macOS**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install django==5.2.7 pandas numpy scikit-learn matplotlib seaborn joblib pillow
```

The supplied quick-start documentation lists these dependencies for the project.

### 4. Run Database Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Placement Officer

Run:

```bash
python manage.py shell
```

Then:

```python
from mainapp.models import PlacementOfficer

PlacementOfficer.objects.create(
    username='admin',
    password='admin123',
    name='System Administrator',
    email='admin@placement.edu',
    mobile='9999999999'
)

exit()
```

### 6. Start the Development Server

```bash
python manage.py runserver
```

### 7. Open the Application

```text
http://127.0.0.1:8000/
```

The project documentation follows the same migration, account creation, and server startup workflow.

---

## 🔑 Demo Login

### Placement Officer

```text
Username: admin
Password: admin123
```

### Student

Register through:

```text
/student_register
```

### HR

HR accounts are created by the Placement Officer.

---

## 🔄 System Workflow

### Student Workflow

```text
Student Registration
        ↓
Student Login
        ↓
Profile Management
        ↓
Upload Resume & Certifications
        ↓
Search Placement Drives
        ↓
Apply for Drive
        ↓
ML Placement Prediction
        ↓
Placement Probability
        ↓
Personalized Suggestions
```

### HR Workflow

```text
HR Account Created
        ↓
HR Login
        ↓
View Placement Drives
        ↓
View Applications
        ↓
Search / Filter Students
        ↓
View Candidate Details
        ↓
Download Resume
```

### Placement Officer Workflow

```text
Officer Login
      ↓
Manage HR Accounts
      ↓
Create Placement Drives
      ↓
Monitor Applications
      ↓
Manage Students
      ↓
View Statistics
      ↓
View ML Analytics
```

The documented workflows cover these three user roles and their major actions.

---

## 🗄️ Database Models

The system contains models for:

* Student
* HR
* Placement Officer
* Placement Drive
* Application
* Certification

The `Student` model stores academic/profile information, while applications connect students with placement drives.

---

## 📊 Feature Importance

According to the project's ML documentation, the major features influencing predictions include:

| Feature                  | Importance |
| ------------------------ | ---------: |
| Degree Percentage        |        28% |
| Employability Test Score |        23% |
| Work Experience          |        18% |
| HSC Percentage           |        12% |
| MBA Percentage           |        10% |

---

## 🔮 Future Enhancements

Possible improvements for future versions:

* Deploy the application to AWS / Render / Railway
* Replace SQLite with PostgreSQL
* Add email notifications
* Improve the ML model using a larger real-world dataset
* Add recruiter analytics
* Add student skill recommendations
* Add resume parsing using NLP
* Add job recommendation system
* Add REST APIs
* Add role-based permissions
* Add Docker support
* Add automated model retraining

---

## 🔒 Security & Production Considerations

Before production deployment:

* Change Django `SECRET_KEY`
* Set `DEBUG = False`
* Configure `ALLOWED_HOSTS`
* Use PostgreSQL/MySQL instead of SQLite
* Configure secure media/static file storage
* Enable HTTPS
* Configure database backups
* Add production logging
* Configure security middleware

These items are included in the project's deployment checklist.

---

## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

* Full-stack web development
* Django framework
* Python programming
* Database design
* CRUD operations
* Authentication & authorization
* Machine Learning
* Random Forest classification
* Data preprocessing
* Model evaluation
* Data visualization
* Responsive UI development
* File upload management
* Multi-role application design

---

## 👩‍💻 Project Highlights

> **Placement Prediction & Management System** combines web development and machine learning to create an intelligent platform for campus placement management.

### Key Highlights

* 🤖 ML-powered placement prediction
* 📊 ~90% reported testing accuracy
* 👨‍🎓 Student placement management
* 👔 HR candidate management
* 👨‍💼 Placement officer administration
* 📄 Resume & certificate management
* 📈 ML performance visualizations
* 💡 Personalized improvement suggestions
* 📱 Responsive user interface

---

## ⭐ If You Like This Project

If you find this project useful, consider giving the repository a ⭐ star!

```text
Built with ❤️ using Python, Django & Machine Learning
```

---

## 📌 Project Information

**Project:** Placement Prediction & Management System
**Backend:** Django
**Language:** Python
**Database:** SQLite
**Machine Learning:** Random Forest Classifier
**Python Version:** 3.8+
**Django Version:** 5.2.7
