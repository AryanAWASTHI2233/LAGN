✅ Problem Statement

Many people struggle to understand whether the symptoms they experience indicate jaundice or a related health issue. They often ignore early signs due to lack of awareness. There is a need for a simple, interactive Python-based system that asks users about common jaundice symptoms, evaluates their responses, calculates a risk score, and provides a meaningful health status. The problem is to design a program that guides users in a basic risk assessment using symptom analysis and visual representation.


---

✅ Scope of the Project

The project focuses on creating a console-based jaundice risk assessment tool using Python.
Its scope includes:

Collecting user input (name and symptom responses).

Checking 10 key symptoms related to jaundice.

Scoring the user’s condition based on their answers.

Categorizing the risk level (Good, Mild, Moderate, High, Critical).

Saving the full report in a text file (report.txt).

Visualizing the health status through a pie chart.

Ensuring ease of use through input validation and modular programming.


The system does not diagnose diseases, but provides a basic preliminary assessment based on symptom count.


---

✅ Target Users

The target users for this project include:

General individuals who want to quickly check if their symptoms may indicate jaundice.

Students or beginners in Python, for learning logic-building, file handling, and visualization.

Basic healthcare awareness programs needing simple assessment tools.

Anyone looking for a preliminary self-check before deciding whether to visit a doctor.



---

✅ High-Level Features

These features summarize what your implemented code can do:

🔹 1. User Information Input

The program asks the user to enter their name and greets them personally.

🔹 2. Symptom-Based Questions

It displays 10 jaundice-related symptoms and takes y/n responses with validation.

🔹 3. Risk Scoring Logic

Each "yes" increases the score. Final score determines the risk level using predefined categories.

🔹 4. Risk Level Determination

The program maps the score to one of the following:

Good (0)

Mild (1–2)

Moderate (3–4)

High (5–6)

Critical (7+)


🔹 5. Report Generation (File Handling)

Saves the user’s:

Name

Selected symptoms

Score

Risk category
into report.txt.


🔹 6. Visual Pie Chart

Displays a Matplotlib pie chart showing:

% Danger (selected symptoms)

% Safe (remaining symptoms)


🔹 7. Modular Class-Based Design

Entire logic organized inside a JaundiceDetector class with separate methods:

get_user_name()

collect_symptoms()

calculate_risk()

save_report()

show_pie_chart()

run()


6️⃣ Modular, OOP-Based Architecture

Core logic organized inside JaundiceDetector class

Easier to extend or modify
