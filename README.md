
---

# Assembly Programs for LCM, Fibonacci, and Factorial Calculations

This repository contains three assembly language programs written for the x86 architecture using MASM syntax. Each program performs a specific mathematical calculation:
1. Least Common Multiple (LCM)
2. Fibonacci sequence calculation
3. Factorial calculation

## Prerequisites

To run these programs, you will need:
- An x86 emulator like [EMU8086](http://www.emu8086.com/) or DOSBox
- MASM assembler or any other compatible assembler for x86 assembly language

## Program Descriptions

### 1.LCM Calculation

**Filename:** `lcm.asm`

**Functionality:** 
This program calculates the Least Common Multiple (LCM) of two single-byte numbers.

- **Inputs:** Hardcoded single-byte values for `num1` and `num2` (example values used are 8 and 17).
- **Outputs:** LCM of the two numbers. The LCM result is displayed on the screen.

**Core Steps:**
- Uses the Euclidean algorithm to calculate the GCD of two numbers.
- Computes the LCM using the formula:  
  \[
  \text{LCM} = \frac{\text{num1} \times \text{num2}}{\text{GCD}}
  \]
- Displays the LCM result.

### 2. Fibonacci Sequence Calculation

**Filename:** `fibonacci.asm`

**Functionality:** 
This program calculates the nth Fibonacci number, where `n` is entered by the user (limited to single-digit values 0–9).

- **Inputs:** User is prompted to enter a single-digit number (0–9).
- **Outputs:** The nth Fibonacci number is displayed on the screen.

**Core Steps:**
- Checks if `n` is 0 or 1, returning 0 or 1, respectively.
- For values of `n` greater than 1, the program iteratively calculates the Fibonacci sequence up to the nth term.
- Displays the result.

### 3. Factorial Calculation

**Filename:** `factorial.asm`

**Functionality:** 
This program calculates the factorial of a number `n`, where `n` is entered by the user (limited to single-digit values 0–9).

- **Inputs:** User is prompted to enter a single-digit number (0–9).
- **Outputs:** The factorial of `n` is displayed on the screen.

**Core Steps:**
- Checks if `n` is 0, as 0! = 1 by definition.
- For values of `n` greater than 0, the program iteratively multiplies the values from 1 up to `n` to compute the factorial.
- Displays the result.

## How to Assemble and Run

1. Open the desired `.asm` file in your assembler or emulator.
2. Assemble the file to produce an executable.
3. Run the executable. Follow the prompts in programs requiring user input.

## Code Structure

Each program follows a similar structure:
1. **Data Segment:** Defines variables, messages, and storage for results.
2. **Code Segment:** Contains the main logic, procedures for calculations, and display functions.
3. **Procedures:** Each program has reusable procedures for specific tasks (e.g., calculating LCM, Fibonacci, and factorial values, and printing numbers).

### Helper Functions
- **print_number:** A common subroutine in each program that converts a 16-bit number to ASCII characters for display.

## Example Usage

Here are example outputs for each program, assuming the inputs given:

- **LCM Calculation**  
  Input values: `num1 = 8`, `num2 = 17`  
  Output:  
  ```
  LCM is: 136
  ```

- **Fibonacci Calculation**  
  User input: `5`  
  Output:  
  ```
  The 5th Fibonacci number is: 5
  ```

- **Factorial Calculation**  
  User input: `4`  
  Output:  
  ```
  The factorial is: 24
  ```

## Troubleshooting

- Ensure that only valid single-digit values (0–9) are entered when prompted, as these programs assume user input is within that range.
- If results do not display correctly, confirm your emulator settings support DOS interrupts (especially INT 21h for displaying strings and characters).

## License

These programs are open-source and can be freely modified for educational purposes.

---
