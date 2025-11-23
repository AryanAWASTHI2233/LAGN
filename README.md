**Project Title**

Health Symptom Analyzer with Risk Pie Chart


---

**Overview of the Project**

The Health Symptom Analyzer is a Python-based interactive program that evaluates a user’s health risk level based on common symptoms. The user answers a series of yes/no questions, and the system calculates a score to determine their risk category. It also generates a visual pie chart using Matplotlib to show the percentage of “Safe” and “In Danger” conditions. This project demonstrates user input handling, decision-making logic, and data visualization in Python.


---

**Features**

User name input and welcome response

Interactive symptom questionnaire (10 symptoms)

Automatic risk scoring

Health status classification (Fine / Rest Needed / Visit Doctor)

Pie chart visualization of danger vs safe percentage

Clean modular code using functions

Beginner-friendly and easy to run



---

**Technologies / Tools Used**

Python 3.x

Matplotlib (for pie chart visualization)

Standard Python libraries: input(), conditionals, lists, loops



---

**Steps to Install & Run the Project**

1. Install Python (if not installed)

Download from: https://www.python.org/downloads/

2. Install Matplotlib

Open terminal / CMD and run:

pip install matplotlib

3. Create a Python file

Save your code as:

health_checker.py

4. Run the project

Open terminal/CMD in the file’s folder and run:

python health_checker.py

5. Follow the on-screen instructions

Enter your name

Answer each symptom using y/n

View your health status and pie chart



---

**Instructions for Testing**

Test the program by entering different combinations of symptoms:

0 symptoms → expect “GOOD, YOU ARE FINE”

1–3 symptoms → expect “TAKE REST”

5 symptoms → expect “AVOID SOCIAL CONTACT, SEE A DOCTOR”

More than 5 → expect “VISIT A DOCTOR QUICKLY”


Test case-insensitivity: y/Y/n/N

Test invalid inputs to ensure the program doesn’t crash

Verify the pie chart always shows correct percentages

Confirm no repeated questions (function called once)

####CODE#####
# JAUNDICE HEALTH INSPECTION
#JAUNDICE INSPECTION TOOL
###[[JAUNDICE HEALTH INSPECTION]]###
import matplotlib.pyplot as plt
def user_name():
     name = input('ENTER NAME:')
     return 'hello ' + name
def get_symptoms():
     symptoms = [
         "Yellowing of eyes/skin",
         "Fever",
         "Vomiting",
         "Loss of appetite",
         "Dark urine",
         "Pale stool",
         "Itching",
         "Stomach pain",
         "chills",
         "weight loss"
     ]
     score = 0
     selected = []
     print("Please answer with y/n:\n")
     for symptom in symptoms:
         ans = input("Experiencing " + symptom + "? (y/n): ")
         if ans.lower() == "y":
          score+=1
          selected.append(symptom)
     if score==0:
         status="GOOD, YOU ARE FINE"
     elif score<=3:
         status="TAKE REST"
     elif score==5:
         status="AVOID SOCIAL CONTACT, TAKE REST, SEE A DOCTOR"
     elif score>5:
         status="VISIT A DOCTOR QUICKLY"
     else:
         status="select a number please"
     return score, status
def show_pie_chart(score, total_symptoms=10):
    danger_pct = (score / total_symptoms) * 100
    safe_pct = 100 - danger_pct
    labels = ["In Danger", "Safe"]
    sizes = [danger_pct, safe_pct]
    colors = ["red", "green"] 
    plt.figure(figsize=(6, 6))
    plt.pie(sizes, labels=labels, colors=colors, autopct="%1.1f%%", startangle=90)
    plt.title("JAUNDICE HEALTH INSPECTION (Danger vs Safe)")
    plt.tight_layout()
    plt.show()
print(user_name())
score, status=get_symptoms()
print('\nStatus:, status')
print('Score:', score)
show_pie_chart(score)
########################################################################
