# Network-honeypot

A simple honeypot that simulates FTP, SSH, HTTP, and HTTPS services to detect and log potential attacks. Based on the [FreeCodeCamp tutorial](https://www.freecodecamp.org/news/build-a-honeypot-with-python/).

## What it does

Listens on ports 21, 22, 80, and 443, pretends to be real services, and logs all connection attempts and attacker commands.

## Files/Folders

- `setup.py` - Main honeypot
- `simulator.py` - Attack simulator for testing
- `logs.py` - Analyzes collected logs
- `socket_prog` - To understand socket programming

## Usage

**Run the honeypot:**
```bash
python setup.py
```

**Test with simulator:**
```bash
python simulator.py
```

**Custom simulation:**
```bash
python simulator.py --intensity high --duration 600
```

## Logs

Activity is logged to `honeypot_logs/honeypot_YYYYMMDD.json` in JSON format:
```json
{
  "timestamp": "2024-12-02T10:30:45.123456",
  "remote_ip": "192.168.1.100", 
  "port": 22,
  "data": "admin:password123"
}
```

## ⚠️ Security Warning

**Educational use only!** Run in isolated environment (VM recommended). Never run as root or on production systems.

## Requirements

- Python 3.6+
- No external dependencies
