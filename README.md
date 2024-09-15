# CVE-2022-35914 Checker

This Python script is designed to check for vulnerabilities related to CVE-2022-35914. It provides a command-line interface to execute commands on target URLs and analyze the command output to detect potential vulnerabilities associated with CVE-2022-35914.

## Features

- Execute a specified command on a single URL or multiple URLs.
- Supports multithreading for faster processing.
- Customizable retry mechanism for handling request failures.
- Allows passing custom headers.
- Simple and clear output: indicates if a target is vulnerable or not.
- Verbose mode to show detailed information on requests and retries.

## Usage

```
Options:
--------
- `-u`, `--url`: Single target URL.
- `-f`, `--file`: File containing target URLs.
- `-c`, `--cmd`: Command to execute (required).
- `-v`, `--verbose`: Enable verbose output for detailed request information.
- `--headers`: Custom headers in the format `key:value`.
- `--retry`: Number of retry attempts if a request fails (default: 1).
- `--threads`: Number of concurrent threads to use (default: 5).
```

## Installation
1. Clone the repository:
```
git clone https://github.com/joelindra/htmlawedchekcer/
```
2. Navigate to the project directory:
```
cd htmlawedchekcer
```

## Dependencies
Python 3.x
Requests library (pip install requests)

## Contribution
Contributions are welcome! Feel free to fork the repository and submit pull requests for new features, improvements, or bug fixes related to CVE-2022-35914 vulnerability checking.
