# PHP CLI Example Application

This repository contains a **minimal PHP command-line application** designed for educational purposes.
It demonstrates how to structure a small PHP project, separate configuration and logic, and run scripts from the terminal.

The project intentionally avoids frameworks, databases, and frontend technologies to keep the focus on **core PHP concepts**.

The project is composed of the following files: app.php, config.php, and lib.php.

The app.php file contains the core of our small program: it loads the lib.php file containing the functions used by the program; it loads the config.php file, which contains the configuration data in an associative array; through conditional statements, it recognizes the commands and options entered by the user and executes the functions associated with them.

The config.php file returns an associative configuration array and enables strict type checking (useful to avoid “silent” errors).

The lib.php file is the internal library of the program and collects the “support” (helper) functions used by the CLI app.

---

## Requirements

- PHP 7.4 or higher (tested with PHP 8.x)
- Command-line access (Windows, Linux, macOS)

Verify PHP installation:

```bash
php -v
```

---

## Project Structure

```text
.
├── app.php        # Application entry point
├── config.php     # Configuration values
├── lib.php        # Helper functions
└── README.md
```

---

## How to Run

Clone the repository and move into the project directory:

```bash
git clone <repository-url>
cd <repository-directory>
```

Run the application using the PHP CLI:

```bash
php app.php
```

---

## Example Output

A typical execution produces output similar to:

```text
Avvio applicazione...
Configurazione caricata correttamente.
Risultato dell'elaborazione: 42
Fine esecuzione.
```

(The exact output depends on the values defined in `config.php`.)

---

## Configuration

The file `config.php` contains configuration constants used by the application.

Example:

```php
define('BASE_VALUE', 10);
```

Changing configuration values will affect the final output when running `app.php`.

---

## Help

The help command can be invoked by passing `-h`, `--help`, or `help` as an argument.

When executed, it displays the main information about the application, including the application name and the current version.

It then shows the list of available commands, along with a brief description of their purpose:
- `audit:ping`: checks whether the application is running correctly (health check)
- `audit:log`: records an audit event
- `audit:whoami`: displays the current user

For each command, any supported arguments and their usage are also indicated.

## Educational Purpose

This repository is intended to be used for:

- learning basic PHP syntax and execution flow;
- understanding file inclusion (`require_once`);
- practicing small, controlled code changes;
- collaborating via Git (branches, merges, conflict resolution).

It is well suited for beginner courses and workshops.

---

## License

This project is provided for educational use.  
No warranty is expressed or implied.
