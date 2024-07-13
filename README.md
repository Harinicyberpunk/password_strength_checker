

# Password Strength Checker

This is a Python-based Password Strength Checker that uses the Tkinter library to create a simple graphical user interface (GUI). The program checks the strength of a given password and provides feedback on how to improve it. The strength is evaluated based on the length, complexity, and commonality of the password.

## Features

- Checks password length
- Checks for the presence of lowercase letters, uppercase letters, digits, and special characters
- Compares the password against a list of common passwords
- Calculates the entropy of the password
- Provides visual feedback on the password strength
- Offers suggestions to improve password strength

## Requirements

- Python 3.x
- Tkinter library (usually included with Python installations)
- A text file containing common passwords (`common_passwords.txt`)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/password-strength-checker.git
   cd password-strength-checker
   ```

2. Ensure you have Python 3 installed. You can download it from [python.org](https://www.python.org/downloads/).

3. Install Tkinter if it's not already included in your Python installation:
   ```sh
   pip install tk
   ```

4. Make sure you have a `common_passwords.txt` file in the same directory as the script. This file should contain a list of common passwords, one per line.

## Usage

1. Run the script:
   ```sh
   python password_strength_checker.py
   ```

2. A GUI window will appear. Enter your password in the input field and click the "Check Strength" button.

3. The program will display the strength of your password, provide feedback, and show the calculated entropy.

## Example

```python
# Define the full path to the common passwords file
common_passwords_path = 'C:\\path\\to\\your\\common_passwords.txt'

# Load common passwords
try:
    with open(common_passwords_path, 'r') as file:
        common_passwords = set(file.read().splitlines())
except FileNotFoundError:
    messagebox.showerror("File Not Found", f"The file {common_passwords_path} does not exist.")
    common_passwords = set()
```

Make sure to replace the `common_passwords_path` variable with the actual path to your `common_passwords.txt` file.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
