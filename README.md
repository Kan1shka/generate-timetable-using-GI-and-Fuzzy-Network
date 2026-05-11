This project leverages a hybrid architecture combining Genetic Algorithms (GA) and Fuzzy Logic to automatically generate conflict-free academic schedules. 
It strict-enforces physical scheduling constraints while smartly optimizing for human-centric preferences like teacher workload balance.

🌟 Key Features (Version 2)
Dynamic Time Mapping: Uses a comprehensive Day + Slot + Time label system instead of basic slot IDs.

Visual Grid Output: Generates colour-coded, ready-to-print timetable grid charts.

Conflict Checker Engine: Provides a full post-run validation report detailing any residual clashes.

Enhanced Mutation Operators: Features 5 distinct mutation actions, including a simultaneous day_slot swap to escape local optima faster.

Rich Performance Metrics: Tracks 8 specific metrics, including convergence generation and average fitness gain per generation.

Advanced Visualizations: Outputs shaded fitness graphs, workload bar charts, and section occupancy heatmaps.

🧠 Core Logic
The system balances two types of constraints to find the optimal schedule:

1. Genetic Algorithm (Hard Constraints)

Teacher Clashes: Ensures a teacher is not scheduled for two classes at the same time.

Room Clashes: Ensures two sections are not assigned the same room simultaneously.

Section Clashes: Ensures a student section does not have overlapping subjects.

Daily Caps: Strictly limits maximum classes per teacher per day (configurable, default is 4).

2. Fuzzy Logic Module (Soft Constraints)

Workload Balance: Penalizes schedules where classes are unevenly distributed among the teaching staff.

Preference Satisfaction: Rewards schedules that place classes in a teacher's preferred time slots.

Consecutive Lectures: Minimizes back-to-back classes to reduce teacher fatigue.

📂 Dataset Requirements
The system requires an Excel dataset named dataset_for_timetable.xlsx containing the following four sheets:

Teachers: Teacher_ID, Subjects, Availability, Max_Classes_Per_Day, Preferred_Slots

subjects: Subject_Name, Type (Theory/Lab), Classes_Per_Week

Rooms: Room_ID, Type (Class/Lab)

sections: Section_ID, Subjects (comma-separated list)

🛠️ Tech Stack & Dependencies
Language: Python 3.10+

Libraries: pandas, numpy, openpyxl

Soft Computing: scikit-fuzzy (with built-in manual fallback)

Visualization: matplotlib, seaborn

🚀 Step-by-Step Execution
Environment: Open the timetable_system (1).ipynb file in Google Colab or Jupyter Notebook.

Install Dependencies: Run the first cell to install required libraries (pip install pandas openpyxl scikit-fuzzy numpy matplotlib seaborn).

Upload Data: Run Step 1 and upload your properly formatted dataset_for_timetable.xlsx file when prompted.

Configure Parameters (Optional): Adjust hyperparameters in Step 3 (e.g., POP_SIZE, NUM_GENERATIONS, MUTATION_RATE, START_TIME).

Run All: Execute the remaining notebook cells sequentially.

Download: The final step will automatically download all generated assets.
