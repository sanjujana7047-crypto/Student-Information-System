Student Information Management System (C Language)
|| Overview

This project is a Student Information Management System written in C, designed to perform common student record operations such as adding, updating, searching, deleting, sorting, and managing attendance.

It also maintains a permanent record by storing all data in external text files (Student.txt and Deleted_details.txt) — even after the program exits.

|*| Features

| Add New Student

Enter roll number, name, course, marks, academic record, and attendance.

Automatically saves data to Student.txt.

| Update Student Information

Modify an existing student’s details using their roll number.

| Show All Students

Displays all current student records in a tabular format.

| Search Student

Search by roll number or name.

| Delete Student

Moves a student's record from Student.txt to Deleted_details.txt.

| Show Deleted Students

View all deleted student details.

| Permanent Delete

Permanently removes a record from Deleted_details.txt.

| Sort Students

Sorts all students by roll number and updates the file.

| Mark Attendance

Updates attendance values for all students interactively.

| Persistent Data Storage

Data automatically saved and loaded from files:

Student.txt → Active student records

Deleted_details.txt → Deleted student records

||#|| File Structure
** Student_Information_System/
│
├── main.c                # Main C source file (this code)
├── Student.txt           # Automatically created file for student data
├── Deleted_details.txt   # Automatically created file for deleted students
└── README.md             # This documentation

|| How It Works

Data Structure

typedef struct Student {
    int roll;
    char name[50];
    char course[50];
    float marks;
    char academic_record[50];
    int attendance;
} student;


Storage Format (Student.txt)

Roll,Name,Course,Marks,Academic Record,Attendance


Deleted Records

When a student is deleted, the record moves to Deleted_details.txt.

You can later permanently remove them from there.

|=| How to Compile and Run
|| Using GCC
gcc main.c -o student_system
./student_system

|*| Using Code::Blocks or Dev-C++

Create a new console project.

Copy the entire code into main.c.

Build and Run.

|!| Menu Operations
Option	Operation Description
1	Add new student
2	Update student details
3	Show all student information
4	Search student (by roll/name)
5	Delete student details
6	Permanently delete record
7	Show deleted students
8	Sort students by roll number
9	Mark attendance
0	Save and Exit
|| Data Persistence

Every operation automatically updates the relevant file.

When you restart the program, data is reloaded from the files using:

Load_from_file()

Load_deleted_file()

! Important Notes

Roll numbers must be unique.

Avoid using extra spaces when searching by name.

Files (Student.txt, Deleted_details.txt) are created automatically if not found.

The maximum number of students (MAX_STUDENT) = 100.

|@| Author

Sanjib Jana, Mim, Harsh Upadhyay & Debmalya Bachaspati
\\ Project Developed in C Language
\\ For learning and practice in file handling, structure, and data management.
