📌 Project Title

Jaundice Risk Predictor – Symptom-Based Health Assessment (CLI Application)


---

📌 Overview

The Jaundice Risk Predictor is a simple Python command-line application designed to analyze user-reported symptoms and estimate the risk level of jaundice.
The program interacts with the user, collects their symptoms, calculates a risk score, and generates a final health status.
It also saves a detailed report to a text file and visualizes the risk distribution using a pie chart.

This project demonstrates Python fundamentals like conditionals, loops, file handling, user input, and data visualization using matplotlib.


---

📌 Features

✔ Interactive CLI symptom checker
✔ User-friendly yes/no based input system
✔ Risk scoring algorithm
✔ Five-level jaundice risk prediction
✔ Automatic report generation (saved in report.txt)
✔ Visual pie chart showing safe vs danger zone
✔ Modular code with clean class-based architecture
✔ Error handling for file creation issues


---

📌 Technologies Used

Technology	Purpose

Python 3	Core programming language
matplotlib	To generate pie-chart visualization
File I/O (Text File)	To store health reports
OOP (Classes & Methods)	To structure logic cleanly



---

📌 Steps to Install and Run

1. Install Python

Make sure Python 3.8+ is installed on your system.

Check using:

python --version

2. Install matplotlib

Run:

pip install matplotlib

3. Download the files

Ensure your project folder contains:

main.py
detector.py

4. Run the program

Open terminal / cmd inside the project folder and type:

python main.py

5. Follow the instructions

You will be asked:

Your name

For each symptom, type y or n


A pie chart will appear at the end, and a report file will be saved.


---

📌 Instructions for Testing the Project

Here’s how to properly test each part:


---

1. Input Testing

✔ Valid inputs:

Enter name normally

For each symptom, type:

y → Yes

n → No



✔ Invalid input test:

Enter something like yes, 1, or maybe → Program should prompt:
"Invalid input! Please type only y or n."


---

2. Score Calculation Testing

Try different combinations:

Symptoms selected	Expected Score	Expected Risk

0	0	GOOD – Completely Fine
1–2	1–2	Mild
3–4	3–4	Moderate
5–6	5–6	High
7–10	7–10	Critical



---

3. Report Generation Testing

After completion, open report.txt and check:

Name printed correctly

List of symptoms shown

Score correct

Risk level correct

No formatting errors



---

4. Pie Chart Testing

Run the program multiple times:

With low symptoms → green part must be bigger

With high symptoms → red part must be bigger

Percentages should match score and remaining safe symptoms



---

5. Error Handling Testing

Try:

Making report.txt read-only

Running without matplotlib installed

Closing the pie chart window early


The program should show proper messages without crashing.


