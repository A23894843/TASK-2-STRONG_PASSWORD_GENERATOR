# Strong Password Generator with Strength Meter

## Overview
This is a Python application that generates strong, random passwords using a graphical user interface (GUI) built with Tkinter. Users can specify the password length, select character sets to include, and view a password strength meter that evaluates the generated password's security.

## Features
- **Customizable Password Length**: Users can input the desired number of characters for the password.
- **Character Set Selection**: Options to include:
  - Uppercase letters (A-Z)
  - Lowercase letters (a-z)
  - Digits (0-9)
  - Special characters (e.g., !@#$%^&*())
- **Password Strength Meter**: Evaluates the password based on:
  - Presence of lowercase letters
  - Presence of uppercase letters
  - Presence of digits
  - Presence of special characters
  - Length ≥ 12 characters
- **Strength Feedback**: Displays strength as:
  - Weak (red, ≤2 criteria)
  - Medium (orange, 3 criteria)
  - Strong (green, 4 criteria)
  - Very Strong (dark green, 5 criteria)
- **Progress Bar**: Visual representation of password strength (0-100%).
- **User-Friendly Interface**: A clean GUI with a light blue theme, buttons for character set selection, and a generate button.
- **Error Handling**: Displays warnings for invalid inputs (e.g., non-numeric length or no character sets selected).
- **Secure Randomization**: Uses Python's `random` module to generate passwords.

## Requirements
- **Python**: Version 3.x
- **Tkinter**: Included with standard Python installations
- **string**: Included with standard Python installations for punctuation checks

## Installation
1. Ensure Python 3.x is installed on your system.
2. No additional libraries are required, as Tkinter and string are part of Python's standard library.
3. Save the script as `password_generator.py`.

## Usage
1. Run the script:
   ```bash
   python password_generator.py
   ```
2. The GUI will open in a maximized window.
3. Enter the desired password length in the input field.
4. Click the buttons to select which character sets to include (Upper-Case, Lower-Case, Digits, Special Character).
5. Click the "Generate Password" button to create a password.
6. The generated password will be displayed, along with its strength level and a progress bar.
7. If an error occurs (e.g., invalid length or no character sets selected), an error message will be displayed.

## Code Structure
- **Imports**:
  - `random`: For password generation
  - `string`: For punctuation checks in strength evaluation
  - `tkinter` and `tkinter.ttk`: For GUI and progress bar
- **Global Variables**:
  - `all_character`: Stores the combined character set based on user selections.
  - `generate`: Stores the generated password.
- **Functions**:
  - `is_l_letter()`: Adds lowercase letters to the character set.
  - `is_u_letter()`: Adds uppercase letters to the character set.
  - `is_digits()`: Adds digits to the character set.
  - `is_special()`: Adds special characters to the character set.
  - `check_strength(password)`: Evaluates password strength based on character types and length.
  - `generate_password()`: Generates the password, updates the strength meter, and handles errors.
- **GUI Elements**:
  - Labels, Entry field, Buttons, Result Label, Strength Label, and Progress Bar for user interaction and feedback.

## Example
- Input: Length = 12, Select Upper-Case, Lower-Case, Digits
- Output: 
  - Generated Password: `kP7nM4xQ9zL2`
  - Strength: Strong (green, progress bar at 80%)

## Limitations
- The script uses the `random` module, which is not cryptographically secure. For high-security applications, consider using the `secrets` module.
- No option to copy the generated password to the clipboard.
- The strength meter is basic and could be enhanced with additional criteria (e.g., checking for repeated characters).

## Future Improvements
- Replace `random` with `secrets` for cryptographically secure password generation.
- Add a "Copy to Clipboard" button.
- Use Checkbuttons instead of Buttons for character set selection to improve UX.
- Add validation for minimum/maximum password length.
- Enhance the strength meter with additional criteria (e.g., checking for common patterns or dictionary words).

## License
This project is open-source and available under the MIT License.
