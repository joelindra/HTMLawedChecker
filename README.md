# HTMLawed Vulnerability Scanner

A powerful and efficient vulnerability scanner specifically designed to detect HTMLawed vulnerabilities in web applications. This tool allows security researchers and penetration testers to quickly identify and verify vulnerable targets using custom payloads and commands.

## Features

- **Fast Multi-threaded Scanning**: Scan multiple targets simultaneously with configurable thread count
- **Advanced Payload Detection**: Execute and test various commands with customizable payloads
- **Flexible Target Input**: Scan individual URLs or read targets from a file
- **Comprehensive Output Options**: Generate reports in text, JSON, or CSV formats
- **Detailed Vulnerability Reporting**: Get clear insights on vulnerable targets
- **HTTP Request Customization**: Add custom headers, cookies, and proxy support
- **Performance Optimization**: Configure retries, timeouts, and delays between requests

## Installation

```bash
# Clone the repository
git clone https://github.com/JoelIndra/htmlawedchecker.git
cd htmlawedchecker

# Install requirements
pip install -r requirements.txt
```

## Dependencies

- Python 3.6+
- rich
- requests

## Usage

### Basic Usage

```bash
# Scan a single URL with a command
python htmlawedchecker.py -u example.com -c "id"

# Scan multiple targets from a file with a command
python htmlawedchecker.py -f targets.txt -c "whoami"

# Use multiple payloads from a file
python htmlawedchecker.py -u example.com --payload-file payloads.txt
```

### Advanced Options

```bash
# Custom headers and timeout
python htmlawedchecker.py -u example.com -c "id" --headers "User-Agent:Mozilla/5.0" "X-Forward-For:127.0.0.1" --timeout 15

# Use a proxy and save results as JSON
python htmlawedchecker.py -f targets.txt -c "uname -a" --proxy http://127.0.0.1:8080 --output json --save results

# Multiple threads with delay between requests
python htmlawedchecker.py -f targets.txt -c "id" --threads 20 --delay 0.5
```

## Command Line Options

### Target Selection
- `-f, --file` - File containing target URLs
- `-u, --url` - Single target URL

### Execution Options
- `-c, --cmd` - Command to execute
- `--payload-file` - File containing multiple commands to try

### Output Options
- `-v, --verbose` - Enable verbose output
- `--output {text,json,csv}` - Output format (default: text)
- `--save SAVE_FILE` - Save results to specified file
- `--quiet` - Silent mode, only display results

### HTTP Options
- `--headers` - Custom headers in the format: key:value
- `--user-agent` - Custom User-Agent string
- `--cookies` - Custom cookies in the format: key=value
- `--proxy` - Proxy to use (e.g., http://127.0.0.1:8080)

### Performance Options
- `--retry` - Number of retries if a request fails (default: 3)
- `--threads` - Number of concurrent threads (default: 5)
- `--timeout` - Request timeout in seconds (default: 10)
- `--delay` - Delay between requests in seconds (default: 0)

## Example Payloads

Create a payload file with commands to execute:

```
id
uname -a
whoami
cat /etc/passwd
ls -la /var/www/html
ps aux
```

## Disclaimer

This tool is meant for security professionals, penetration testers, and researchers to audit their own systems or systems they have permission to test. Do not use this tool against targets without explicit permission. The author is not responsible for any misuse of this software.

## Contributors

- [JoelIndra](https://github.com/JoelIndra) - Creator and maintainer

## License

This project is licensed under the MIT License - see the LICENSE file for details.
