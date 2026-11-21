# 🚀 SlotWise – Constraint-Based Academic Timetable Scheduling System

<p align="center">
  <b>Intelligent Scheduling • Resource Optimization • Academic Automation</b>
</p>

<p align="center">
  An automated academic scheduling platform that generates conflict-aware university timetables by managing course allocations, instructor availability, classroom resources, student batches, and specialized academic constraints.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Streamlit-Frontend-FF4B4B?logo=streamlit&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pandas-Data%20Processing-150458?logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Excel-OpenPyXL-217346?logo=microsoftexcel&logoColor=white"/>
  <img src="https://img.shields.io/badge/Testing-Pytest-0A9EDC?logo=pytest&logoColor=white"/>
</p>

---

## 📌 Overview

**SlotWise** is an intelligent academic timetable scheduling system designed to automate the complex process of university course scheduling and classroom allocation.

Traditional manual timetable preparation involves coordinating multiple constraints, including faculty availability, classroom capacity, laboratory requirements, student batches, course durations, and academic time windows.

SlotWise addresses these challenges through a constraint-based scheduling approach that automates timetable generation while minimizing scheduling conflicts and improving resource utilization.

Originally developed for academic scheduling requirements at **IIIT Dharwad**, the system supports both interactive timetable generation and automated command-line execution.

## ✨ Key Features

### 1. Intelligent Timetable Generation
- Automatically generates academic timetables across multiple days and time slots.
- Handles multiple courses, semesters, departments, and student batches.
- Supports pre-semester and post-semester scheduling.

### 2. Constraint-Based Scheduling
- Instructor availability and scheduling constraints.
- Classroom capacity and facility requirements.
- Dedicated laboratory scheduling.
- Lunch breaks and restricted academic time windows.
- Separate scheduling windows for minor programs.
- Lecture, tutorial, and practical session duration requirements.
- Sequential scheduling for student batches.

### 3. Automated Classroom Allocation
- Assigns suitable classrooms based on course requirements.
- Considers room capacity and classroom type.
- Supports separate classroom and laboratory allocation.
- Prevents overlapping room assignments.

### 4. Interactive Web Interface
- Built using Streamlit.
- Upload course, classroom, and minor program Excel files.
- Generate timetables through an interactive interface.
- Download generated scheduling reports.

### 5. Command-Line Scheduling
- Supports non-interactive timetable generation.
- Processes input files directly from the input directory.
- Automatically saves generated Excel reports.
- Suitable for batch processing and automated workflows.

### 6. Excel-Based Reporting
- Generates structured Excel timetables.
- Creates separate sheets for individual student batches.
- Uses color-coded schedules for better readability.
- Highlights lunch breaks, free periods, and minor program sessions.

### 7. Input Validation & Testing
- Validates input Excel files before scheduling.
- Identifies missing or invalid scheduling information.
- Provides warnings for potential scheduling issues.
- Includes automated tests using Pytest.

---

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| Data Processing | Pandas |
| Excel Processing | OpenPyXL |
| Architecture | Modular Python, OOP |
| Scheduling | Constraint-Based Scheduling |
| Testing | Pytest |
| Version Control | Git, GitHub |

---

## 🏗️ System Architecture

SlotWise follows a modular architecture that separates input processing, validation, scheduling logic, resource allocation, and output generation.

```text
              ┌──────────────────────┐
              │        USER          │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │  Streamlit / CLI     │
              │    Interface         │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │    Input Reader      │
              │                      │
              │ Courses              │
              │ Classrooms           │
              │ Minor Programs       │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │   Data Validator     │
              │                      │
              │ Input Validation     │
              │ Constraint Checks    │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │  Scheduling Engine   │
              │                      │
              │ Course Allocation    │
              │ Time Slot Assignment │
              │ Batch Scheduling     │
              └──────────┬───────────┘
                         │
              ┌──────────┴───────────┐
              ▼                      ▼
    ┌──────────────────┐   ┌──────────────────┐
    │ Room Allocator   │   │ Conflict Checks  │
    │                  │   │                  │
    │ Capacity         │   │ Faculty          │
    │ Room Type        │   │ Classroom        │
    │ Facilities       │   │ Time Slots       │
    └─────────┬────────┘   └─────────┬────────┘
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │   Excel Generator    │
              │                      │
              │ Pre-Semester         │
              │ Post-Semester        │
              └──────────┬───────────┘
                         │
                         ▼
              ┌──────────────────────┐
              │  Generated Timetables│
              │     Excel Reports    │
              └──────────────────────┘
```

---

## ⚙️ Scheduling Workflow

1. **Data Collection:** Import course, classroom, and minor program information from Excel files.
2. **Input Validation:** Verify required columns, data types, and scheduling information.
3. **Resource Filtering:** Identify suitable classrooms and laboratories based on capacity and facility requirements.
4. **Batch Scheduling:** Organize courses according to student batches and academic requirements.
5. **Time Slot Allocation:** Assign available time slots while respecting academic scheduling constraints.
6. **Conflict Management:** Check instructor availability, classroom occupancy, and scheduling restrictions.
7. **Timetable Generation:** Generate structured and color-coded Excel schedules.
8. **Report Export:** Save pre-semester and post-semester timetables for distribution.

---

## 📂 Project Structure

```text
SlotWise/
│
├── input/
│   ├── course_data.xlsx
│   ├── classroom_data.xlsx
│   └── minor.xlsx
│
├── output/
│   ├── pre_semester_timetables.xlsx
│   └── post_semester_timetables.xlsx
│
├── src/
│   └── timetable_scheduler/
│       ├── __init__.py
│       ├── config.py
│       ├── models.py
│       ├── input_reader.py
│       ├── validator.py
│       ├── scheduler.py
│       ├── room_allocator.py
│       └── excel_writer.py
│
├── tests/
│   ├── test_input_reader.py
│   ├── test_room_allocator.py
│   └── test_scheduler.py
│
├── app.py
├── run_scheduler_noninteractive.py
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/Ctrl-Alt-Survive/AutomatedTimeTable.git

cd AutomatedTimeTable
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv venv

venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv venv

source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch the Web Application

```bash
streamlit run app.py
```

Open the application in your browser:

```text
http://localhost:8501
```

### 5. Run Using Command Line

For non-interactive scheduling:

```bash
python run_scheduler_noninteractive.py
```

The system reads input files from the `input/` directory and generates Excel timetables inside the `output/` directory.

---

## 📊 Input Data Requirements

SlotWise uses Excel-based input files for academic scheduling.

### Course Data – `course_data.xlsx`

| Column | Description |
|---|---|
| Course Code | Unique course identifier |
| Course Name | Full course name |
| Semester | Academic semester |
| Department | Department name |
| LTPSC | Lecture, Tutorial, Practical, Session and Credit structure |
| Credits | Course credits |
| Instructor | Assigned faculty members |
| Registered Students | Number of enrolled students |
| Elective | Indicates elective course |
| Half Semester | Indicates half-semester course |

### Classroom Data – `classroom_data.xlsx`

| Column | Description |
|---|---|
| Room Number | Unique classroom identifier |
| Type | Classroom or Laboratory |
| Capacity | Maximum student capacity |
| Facilities | Available room facilities |

### Minor Program Data – `minor.xlsx`

| Column | Description |
|---|---|
| Program Name | Minor program name |
| Registered Students | Number of enrolled students |

---

## ⏰ Scheduling Configuration

Scheduling parameters can be customized through:

`src/timetable_scheduler/config.py`

The configuration supports:

- Working hours and academic time windows.
- Dedicated minor program slots.
- Lunch break restrictions.
- Lecture, tutorial, and laboratory durations.
- Minimum gaps between consecutive sessions.

Example configuration:

```python
WORK_START = time(7, 30)
WORK_END = time(20, 0)

MINOR_WINDOWS = [
    (time(7, 30), time(9, 0)),
    (time(18, 30), time(20, 30)),
]

REGULAR_WINDOW = (
    time(9, 0),
    time(18, 30)
)

LUNCH_START = time(12, 30)
LUNCH_END = time(14, 0)

TUTORIAL_DURATION = 60
LECTURE_DURATION = 90
LAB_DURATION = 120
MINOR_DURATION = 90
```

---

## 📤 Generated Outputs

SlotWise generates two primary Excel reports.

### 1. Pre-Semester Timetables

- Contains schedules for the first half of applicable courses.
- Separate worksheets for individual batches and sections.
- Includes course codes, instructor details, room assignments, and time slots.

### 2. Post-Semester Timetables

- Contains schedules for the second half of applicable courses.
- Maintains the same structured Excel format.

### Color-Coded Scheduling

| Color | Meaning |
|---|---|
| Pastel shades | Regular academic sessions |
| Yellow | Lunch breaks |
| Light Gray | Free periods |
| Light Blue | Minor program sessions |

---

## 🧪 Testing

Run the complete test suite:

```bash
pytest tests/ -v
```

Run individual test modules:

```bash
pytest tests/test_scheduler.py -v

pytest tests/test_room_allocator.py -v

pytest tests/test_input_reader.py -v
```

Run tests with coverage:

```bash
pytest tests/ --cov=src/timetable_scheduler
```

---

## 🎯 Key Engineering Concepts

| Concept | Application |
|---|---|
| Constraint Satisfaction | Managing academic scheduling restrictions |
| Resource Allocation | Assigning classrooms and laboratories |
| Scheduling Algorithms | Allocating courses to available time slots |
| Object-Oriented Programming | Modular course, room, and scheduling models |
| Data Validation | Ensuring reliable Excel input processing |
| Conflict Detection | Preventing overlapping resource assignments |
| Automation | Generating academic schedules with minimal manual intervention |

---

## 🔮 Future Enhancements

- [ ] Advanced timetable optimization using Genetic Algorithms.
- [ ] Constraint Programming using Google OR-Tools.
- [ ] Automated conflict resolution and rescheduling.
- [ ] Interactive timetable visualization.
- [ ] Faculty workload balancing.
- [ ] Database integration for persistent academic data.
- [ ] Cloud deployment and multi-institution support.
- [ ] Timetable comparison and optimization analytics.

---

## 📜 License & Attribution

This project was developed for academic timetable automation at IIIT Dharwad.

Please refer to the repository for licensing and contribution information.

---

<p align="center">
  <b>SlotWise – Smarter Scheduling. Better Resource Utilization.</b>
</p>

<p align="center">
  ⭐ If you find this project useful, consider starring the repository!
</p>
