# password_manager

# Password Manager 🛡️

A simple Python-based password manager that stores account credentials securely, allowing you to easily retrieve and manage your passwords via the command line.

---

## Features

- **Retrieve Passwords**: Quickly copy a password to your clipboard by providing the account name.
- **Add New Accounts**: Dynamically add new accounts and passwords.
- **Persistent Storage**: Save and load your passwords from a file for easy access across sessions.

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/svedant1207/password_manager.git
   cd password-manager
   ```

2. **Install Dependencies**:
   Ensure you have Python 3.7+ installed and run:
   ```bash
   pip install pyperclip
   ```

---

## Usage

1. **Run the Script**:
   ```bash
   python password.py [account_name]
   ```

2. **Examples**:
   - Retrieve an existing password:
     ```bash
     python password.py email
     ```
     If the account exists, the password is copied to your clipboard.

   - Add a new account:
     Modify the `password.py` script to include:
     ```python
     PASSWORDS['new_account'] = 'new_password'
     ```

3. **Save to a File**:
   - To persist data:
     ```python
     import json
     with open('passwords.json', 'w') as file:
         json.dump(PASSWORDS, file)
     ```
   - To load the saved passwords:
     ```python
     try:
         with open('passwords.json', 'r') as file:
             PASSWORDS = json.load(file)
     except FileNotFoundError:
         PASSWORDS = {}
     ```

---

## File Structure

```
password-manager/
├── password.py        # Main script for the password manager
├── passwords.json     # File to store the passwords persistently
└── README.md          # Documentation file
```

---

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request on GitHub.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to modify this template and add your repository’s specific details!
