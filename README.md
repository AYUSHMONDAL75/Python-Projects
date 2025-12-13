Student Result Management System
A Python-based GUI application designed for hs student marks calculate(ex: Natra High School (H.S)) to calculate student results, determine grades, and store data automatically in an Excel file.

📋 Project Description
This application provides a user-friendly interface for teachers or administrators to input student marks for six subjects. It automatically calculates the Total Marks, Percentage, and Division (Grade) based on the inputs. All records are saved to a local Excel file (result.xlsx) for future reference.

✨ Features
Graphical User Interface (GUI): Built with tkinter, featuring a centered, non-resizable window.

Subject Input: Fields for Bengali, English, Physics, Chemistry, Mathematics, and Biology.

Automatic Calculation: Instantly computes Total and Percentage.

Grading Logic:

70% +: STAR (*)
60% - 69%: 1st Division
50% - 59%: 2nd Division
40% - 49%: 3rd Division
Below 40%: Fail
Data Persistence: Automatically creates and appends data to result.xlsx.
Validation: Checks if the percentage exceeds 100% (invalid entry).

🛠️ Prerequisites
To run this project, you need Python installed on your system along with the openpyxl library (used for Excel operations).

Required Libraries:
tkinter (Usually comes pre-installed with Python)

openpyxl
⚙️ Installation & Setup
Install Python: Ensure Python 3.x is installed.
Install Dependencies: Run the following command in your terminal/command prompt to install the Excel handler:

Bash
pip install openpyxl
Run the Application: Run the Python script:

Bash
python your_script_name.py
🚀 How to Use
Launch the application.

Enter the Student Name.
Enter the marks obtained in the Subject Numbers fields (Bengali, English, Physics, Mathematics, Chemistry, Biology).
Click the "Result" button at the bottom.
A pop-up message will display the summary (Total, Percentage, and Division).
The data is automatically saved to a file named result.xlsx in the same folder.

📂 File Structure
main.py (The source code)
result.xlsx (Generated automatically upon first run to store data)
