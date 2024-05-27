# CVE-2022-35914 Checker

This Python script is designed to check for vulnerabilities related to CVE-2022-35914. It provides a command-line interface to execute commands on target URLs and analyze the command output to detect potential vulnerabilities associated with CVE-2022-35914.

## Features

- Execute commands on single or multiple target URLs.
- Check for vulnerabilities related to CVE-2022-35914 in the command output.
- Color-coded output for easy vulnerability identification.
- Handle target URLs from a file.
- Supports customizable command execution and error handling.

## Usage

```
./exploit.py -f <TARGET_FILE> -u <URL> -c <CMD>
-f, --file: Specify a file containing target URLs.
-u, --url: Specify a single target URL.
-c, --cmd: Specify the command to execute (required).
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
