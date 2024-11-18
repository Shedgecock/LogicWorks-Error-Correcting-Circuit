# LogicWorks-Error-Correcting-Circuit
Design of a circuit that is able to detect and correct errors in 8 bits of transmitted data.
# Lab 2: Error Correcting Code (ECC) System
## Team Members and Contributions
1. **Teague Sangster** - Implemented the **ECC Generator** (Part 1):
   - Designed the circuit for calculating the 5 parity bits using XOR gates.
   - Created the device symbol for the ECC Generator and ensured it outputs a 13-bit data vector.

2. **Sean Hedgecock** - Implemented the **13-bit Data Transmission Bus** (Part 2):
   - Developed the circuit for simulating data transmission and introduced error inputs using XOR gates.
   - Created the device symbol for the Data Bus and tested it with error simulation switches (E1-E13).

3. **Noah Bakayou** - Implemented the **ECC Detector at Main Memory** (Part 3):
   - Designed the circuit for detecting and correcting single-bit errors using syndrome calculation.
   - Created the device symbol for the ECC Detector and implemented error status logic for "0," "C," and "E" outputs.

## Submission Package
The enclosed files in the submission package are as follows:

1. **README.txt** - This file, containing group member names, contributions, and file descriptions.

2. **Library File (.clf)** - Contains all the device symbols for the ECC Generator, Data Transmission Bus, and ECC Detector circuits. It allows you to import the symbols into LogicWorks.

3. **ECC3.cct** - The circuit file for Part 1:
   - Calculates the 5 parity bits (P1-P5) for an 8-bit data input.
   - Outputs a 13-bit vector consisting of the data bits and parity bits.
   - This file should be loaded first to test the ECC generation.
   - ![Alt text](ECC3.png?raw=true "Optional Title")

4. **13-bit Data Transmission.cct** - The circuit file for Part 2:
   - Simulates the transmission of the 13-bit data vector.
   - Allows the user to introduce errors using switches (E1-E13) to flip bits in the transmitted data.
   - Outputs the modified 13-bit vector, which is used as input for the ECC Detector.
   - ![Alt text](13-bit%20Data%20Transmission.png?raw=true "Optional Title") 

5. **Part 3.cct** - The circuit file for Part 3:
   - Detects and corrects single-bit errors using Hamming Code.
   - Displays the corrected data and indicates the error status (0 for no error, C for single-bit correction, E for multiple-bit errors).
   - Outputs the corrected 8-bit data and the error status.
   - ![Alt text](Decoder.png?raw=true "Optional Title")
     
   - ![Alt text](Main%20Memory.png?raw=true "Optional Title") 

6. **Main.cct** - The integrated circuit file:
   - Connects the ECC Generator, Data Transmission Bus, and ECC Detector together.
   - Allows for end-to-end testing of the ECC system.
   - Displays the final output data on two hexadecimal displays and the error status on a third hexadecimal display.
   - ![Alt text](Main%20Circuit.png?raw=true "Optional Title")

## Usage Instructions
1. Load the **Main.cct** file in LogicWorks.
2. Input two hexadecimal numbers as the 8-bit data input in the ECC Generator.
3. Use the switches (E1-E13) in the Data Transmission Bus to simulate errors during transmission.
4. Observe the final output on the hexadecimal displays:
   - The first two displays show the 8-bit data output.
   - The third display shows the error status (0, C, or E).
5. Test the circuit with different input data and error conditions to verify functionality.

## Testing Notes
- No error: Set all error switches (E1-E13) to 0. The output data should match the input data, and the error status should display "0."
- Single-bit error: Set one error switch (e.g., E3) to 1. The output data should be corrected, and the error status should display "C."
- Double-bit error: Set two error switches (e.g., E2 and E5) to 1. The output data will not be corrected, and the error status should display "E."

## Conclusion
  Our original plan for this project was to divide the work into three distinct parts and combine them in the **Main.cct** file for final testing. However, this approach did not go as expected. Although each team member developed their part as planned, we faced significant challenges when integrating the components. We decided to come together as a team and troubleshoot the entire circuit collectively. After several modifications and extensive testing, we were able to get the ECC system working correctly. A problem we did face is corrupted files. In order to mitigate this we created several new **.clf** libary files. Unfortunately, this lead to the original **.clf** being lost. Our group decided to share files with each other only using the more robust **.cct** files. This project showed the importance of teamwork and demonstrated that collaboration can be far more effective than working in alone. We gained valuable experience in problem-solving, circuit design, and working together as a cohesive unit.
  
---

End of README
