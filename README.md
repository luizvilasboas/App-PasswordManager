# App-PasswordManager

> A command-line password manager written in Perl for securely storing and managing your passwords.

## About the Project

`App::PasswordManager` is a CLI tool that allows users to securely add, list, edit, remove, and copy passwords. All passwords are encrypted using PBKDF2 and stored in a local JSON file in the user's home directory, ensuring your data remains secure and private.

Key features include:
*   **Add Password**: Add a new password entry for a specific login.
*   **List Passwords**: Display a list of all stored logins.
*   **Edit Password**: Edit the password for an existing login.
*   **Remove Password**: Delete a password entry.
*   **Copy to Clipboard**: Copy a password to the clipboard for easy use.
*   **Encrypted Storage**: Passwords are securely stored in an encrypted format.

## Tech Stack

The main technologies and libraries used in this project are:

*   [Perl](https://www.perl.org/)
*   [Crypt::PBKDF2](https://metacpan.org/pod/Crypt::PBKDF2)
*   [File::HomeDir](https://metacpan.org/pod/File::HomeDir)
*   [JSON](https://metacpan.org/pod/JSON)

## Usage

Below are the instructions for you to set up and run the project.

### Prerequisites

You need to have the following software installed:

*   [Perl](https://www.perl.org/get.html)
*   [cpanm](https://metacpan.org/pod/App::cpanminus) (a common Perl module installer)

### Installation and Setup

You can install the application via MetaCPAN (recommended) or manually.

**1. Install from MetaCPAN**
```bash
cpanm install App::PasswordManager
```

**2. Manual Installation**
```bash
# Clone the repository
git clone https://github.com/luizvilasboas/App-PasswordManager.git
cd App-PasswordManager

# Install dependencies
cpanm --installdeps .

# Build and install the module
perl Makefile.PL
make
sudo make install
```

### Workflow

After installation, you can use the `password_manager` command-line tool:

*   **Add a new password:**
    ```bash
    password_manager --add "my-email@example.com" "mysecretpassword"
    ```
*   **List all stored logins:**
    ```bash
    password_manager --list
    ```
*   **Edit a password:**
    ```bash
    password_manager --edit "my-email@example.com" "newpassword"
    ```
*   **Remove a password:**
    ```bash
    password_manager --remove "my-email@example.com"
    ```
*   **Copy a password to the clipboard:**
    ```bash
    password_manager --copy "my-email@example.com"
    ```

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
