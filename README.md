# CVE-2022-35914 Checker

This Python script is designed to check for vulnerabilities related to CVE-2022-35914. It provides a command-line interface to execute commands on target URLs and analyze the command output to detect potential vulnerabilities associated with CVE-2022-35914.

![image](https://github.com/user-attachments/assets/40cae1c0-6cb1-404c-8e54-f63e7e27585a)


## Features

```
--file: Provides a file with a list of URLs to check.
--url: Specifies a single URL to check.
--cmd: Provides a command to run on the target (required).
--headers: Lets you add custom headers for requests.
--retry: Sets how many times to retry if a request fails (default: 1).
--threads: Specifies how many tasks to run in parallel (default: 5).
--timeout: Sets the time to wait for a response before giving up (default: 10 seconds).
--verbose: Shows more detailed output.
```
## Usage

```
usage: main.py [-h] [-f FILE] [-u URL] [-c CMD] [-v] [--headers HEADERS [HEADERS ...]] [--retry RETRY] [--threads THREADS] [--timeout TIMEOUT]

options:
  -h, --help            show this help message and exit
  -f FILE, --file FILE  File containing target URLs
  -u URL, --url URL     Single target URL
  -c CMD, --cmd CMD     Command to execute
  -v, --verbose         Enable verbose output
  --headers HEADERS [HEADERS ...]
                        Custom headers in the format: key:value
  --retry RETRY         Number of retries if a request fails (default: 1)
  --threads THREADS     Number of concurrent threads (default: 5)
  --timeout TIMEOUT     Request timeout in seconds (default: 10)
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
