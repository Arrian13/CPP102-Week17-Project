Simulated Device Monitoring and Alert System

Student Name: Arrian F. Sadicon  
Student Number: 2601275  
Section: 1CPE-B

Project Description
This project is a simple Python program for monitoring simulated device temperature readings. It stores temperature values and classifies each one as NORMAL, WARNING, or CRITICAL. It can also calculate a summary and show the overall monitoring status. The readings are only for a classroom activity and are not real device-safety standards.

Features
- View all stored temperature readings.
- Add a whole-number reading from 0 to 100.
- Reject empty, non-numeric, negative, and over-100 readings.
- Classify readings as NORMAL, WARNING, or CRITICAL.
- Calculate the total, average, minimum, maximum, category counts, and percentages.
- Display the overall monitoring status.
- Repeat the menu until the user chooses Exit.

Requirements
- Python 3
- No external packages are needed.

How to Run
1. Save `device_monitor.py` inside the `Week17` folder.
2. Open a terminal in that folder.
3. Run this command:

```text
python device_monitor.py

If your computer uses `python3`, run `python3 device_monitor.py` instead.

Sample Output
The following summary was observed by running the program with the initial readings:

```text
MONITORING SUMMARY
------------------
Number of readings : 5
Total of readings : 160
Average temperature : 32.00 °C
Minimum temperature : 28 °C
Maximum temperature : 37 °C

NORMAL : 2 (40.00%)
WARNING : 2 (40.00%)
CRITICAL : 1 (20.00%)

Overall Status: ATTENTION REQUIRED

Test Cases
Ten planned test cases are listed in [test_cases.md](test_cases.md). They cover viewing readings, valid and invalid input, the boundary values 30 °C and 35 °C, the numerical summary, invalid menu choice, and Exit. Run the tests on your own computer and confirm the actual results before submitting.

 Known Limitations
- The readings are simulated and are not collected from a real device or sensor.
- Readings are stored in a list only, so new readings are lost when the program closes.
- The program does not save reports to a file.
- The temperature limits are only for this classroom simulation.

Reflection
I learned how to combine functions, lists, loops, and if statements in one complete program. One important part was checking the user's input before adding it to the list. I also had to make sure that 30 and 35 are both classified as WARNING. I used loops to calculate the total, minimum, and maximum instead of using built-in functions. In the future, I would like to learn how to save the readings so they can still be available after the program closes.

Program Rules
- Below 30 °C: NORMAL
- 30 °C to 35 °C, inclusive: WARNING
- Above 35 °C: CRITICAL
- Valid new readings are whole numbers from 0 to 100, inclusive.
- Overall status is ATTENTION REQUIRED if at least one CRITICAL reading exists; otherwise it is MONITOR if at least one WARNING reading exists; otherwise it is NORMAL.

Function Overview
- `get_initial_readings()` returns the starting list.
- `add_reading()` validates and adds a reading.
- `classify_reading()` returns a category.
- `compute_total()`, `compute_average()`, `find_minimum()`, and `find_maximum()` calculate numerical results.
- `count_category()` counts readings in a category.
- `determine_overall_status()` returns the overall status.
- `display_summary()` displays the calculated report.
- `main()` controls the menu and calls the other functions.

Author
Arrian F. Sadicon — CPP102, Programming Logic and Design

References
- CPP102 Week 17 Lecture and Laboratory Module, Department of Computer Engineering, Pamantasan ng Cabuyao.
- Python Software Foundation. (n.d.). The Python Tutorial. https://docs.python.org/3/tutorial/
- GitHub. (n.d.). Basic writing and formatting syntax. https://docs.github.com/en/get-started/writing-on-github