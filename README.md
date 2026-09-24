# Personal Password Manager

A simple command-line password manager written in Python. The program allows users to:

* Save website passwords
* View saved passwords
* Generate random passwords
* Store password data in a local `passwords.txt` file

> **Security warning:** This project is intended for learning and demonstration purposes. Passwords are stored in plain text and should **not** be used for storing real or sensitive passwords.

## Project Structure

```text
password-manager/
│
├── password_manager.py
├── passwords.txt
└── README.md
```

## Requirements

Before running the project, make sure you have:

* Python 3.8 or newer
* A terminal or command prompt
* Git, if you are cloning the repository from GitHub

The project uses only Python's built-in libraries, so **no external Python packages are required**.

## 1. Clone the Repository

Open a terminal and clone the repository:

```bash
git clone <YOUR_REPOSITORY_URL>
```

Move into the project directory:

```bash
cd password-manager
```

Replace `<YOUR_REPOSITORY_URL>` with the URL of this GitHub repository.

## 2. Check Python Installation

Check that Python is installed:

### Windows

```bash
python --version
```

### macOS / Linux

```bash
python3 --version
```

You should see a Python version such as:

```text
Python 3.11.5
```

If Python is not installed, install Python 3.8 or newer from the official Python website.

## 3. Create a Virtual Environment

A virtual environment is recommended even though this project has no external dependencies.

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

After activation, your terminal should show `(venv)`.

## 4. Install Dependencies

This project does not require any third-party packages.

All functionality uses Python's standard library, including:

* `random`
* `string`

Therefore, there is no `pip install` command required.

If the repository contains a `requirements.txt` file in the future, install its dependencies with:

```bash
pip install -r requirements.txt
```

## 5. Configuration

No additional configuration or environment variables are required.

The program automatically uses:

```text
passwords.txt
```

to store saved passwords.

If the file does not exist when the program starts, the application will create it when the first password is saved.

### Important

Do not commit real passwords or sensitive information to GitHub.

If `passwords.txt` contains personal passwords, add it to `.gitignore`:

```text
passwords.txt
venv/
__pycache__/
```

## 6. Run the Project

From the project directory, run:

### Windows

```bash
python password_manager.py
```

### macOS / Linux

```bash
python3 password_manager.py
```

The application will display a menu similar to:

```text
----- PERSONAL PASSWORD MANAGER -----
1. Save Password
2. View Passwords
3. Generate Password
4. Exit

Enter your choice:
```

## 7. Using the Application

### Save a Password

Select:

```text
1
```

Enter the website and password when prompted.

Example:

```text
Enter your choice: 1
Enter website: example.com
Enter password: mypassword123
Saved!
```

The information will be stored locally in `passwords.txt`.

### View Passwords

Select:

```text
2
```

The program displays the saved website/password pairs.

Example:

```text
example.com : mypassword123
```

### Generate a Password

Select:

```text
3
```

The program generates an 8-character random password containing letters, numbers, and selected special characters.

Example:

```text
Generated Password: a8@K2$mQ
```

### Exit

Select:

```text
4
```

to close the application.

## Data Storage

Saved passwords are stored in the following format:

```text
website:password
```

For example:

```text
example.com:mypassword123
github.com:password456
```

The application loads existing entries from `passwords.txt` when it starts.

## Troubleshooting

### `python: command not found`

Try:

```bash
python3 --version
```

If that works, run the application with:

```bash
python3 password_manager.py
```

### `No such file or directory`

Make sure you are running the command from the project directory:

```bash
cd password-manager
```

Then run the program again.

### Password file does not exist

This is normal. The application creates `passwords.txt` when you save your first password.

## Security Limitations

This is an educational project and is **not a production-grade password manager**.

Current limitations include:

* Passwords are stored in plain text.
* There is no master password.
* There is no encryption.
* Generated passwords use Python's `random` module rather than a cryptographically secure generator.
* Anyone who can access `passwords.txt` can read the stored passwords.

For a production application, passwords should be protected using appropriate encryption, secure key management, and cryptographically secure random generation.

## License

This project is intended for educational purposes.

```
```

