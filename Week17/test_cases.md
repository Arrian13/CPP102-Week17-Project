Test Cases – Simulated Device Monitoring and Alert System

Tested by:  Arrian F. Sadicon  
Date of testing: 18 October 2026  

These tests were run using scripted terminal input with the program in this folder. Run them again on your own computer before submitting.

| Test Case | Input or Action | Expected Result | Actual Result Observed | Pass/Fail |
|---|---|---|---|---|
| TC01 | Choose 1 | Five readings: 28, 31, 35, 37, 29 | Displayed Reading 1: 28 °C and all five readings | Pass |
| TC02 | Choose 2, enter 33 | Reading added successfully | Reading added successfully. | Pass |
| TC03 | Choose 2, enter abc | Rejected; list remains unchanged | Invalid input. Enter a whole number only. | Pass |
| TC04 | Choose 2, enter -5 | Rejected; list remains unchanged | Invalid reading. Enter a value from 0 to 100. | Pass |
| TC05 | Choose 2, enter 120 | Rejected; list remains unchanged | Invalid reading. Enter a value from 0 to 100. | Pass |
| TC06 | Choose 2, enter 30; then choose 3 | 30 °C -> WARNING | 30 °C -> WARNING | Pass |
| TC07 | Choose 3 | 35 °C -> WARNING | 35 °C -> WARNING | Pass |
| TC08 | Choose 4 with initial data | Total 160, average 32.00, minimum 28, maximum 37; status ATTENTION REQUIRED | Total 160; average 32.00 °C; minimum 28 °C; maximum 37 °C; ATTENTION REQUIRED | Pass |
| TC09 | Enter 9 at the menu | Error message appears and menu repeats | Invalid choice message displayed; menu repeated | Pass |
| TC10 | Choose 5 | Exit message appears and program ends | Thank you for using the Device Monitoring System. | Pass |

Bugs Found and Fixed

During checking, I confirmed that the minimum must start from the first reading in the list rather than 0. Starting from 0 would give an incorrect minimum when all readings are above 0. The program uses `minimum = readings[0]` and then compares the other readings in a loop.

Testing Note

The tests above were run in a scripted terminal session. Please repeat them in your own terminal and update this file if your observed results differ.

