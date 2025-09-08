# 1. Port Scanning with Nmap

## Method 1 (In Virtual Machines like Kali Linux)
Tool: nmap (already in Kali).
Target: Metasploitable VM.

### Command examples:

```bash
nmap -sV 192.168.56.101         # Service/version detection
nmap -A 192.168.56.101          # Aggressive scan (OS + services + traceroute)
nmap -p- 192.168.56.101         # Scan all 65k ports

