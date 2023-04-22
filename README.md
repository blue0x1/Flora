# <p align="center">Flora<p/>


Flora is a command-line tool designed to enumerate subdomains for a given domain and identify potential subdomain takeovers. The tool supports multiple modes of operation, including discovery and takeover, and offers several options for customizing the scanning process.
<br>

<p align="center">
  <img src="flora.png" alt="Flora">
</p>



## Features:

- Subdomain discovery using a variety of methods, including brute force, Shodan, VirusTotal, and SecurityTrails.
- Subdomain takeover identification.
- Customizable wordlists for brute force.
- Verbose mode for detailed output.
- Multi-threaded brute force.
- Option to output results to a file.
- Fingerprinting to identify subdomains.
- Support for Assetfinder for subdomain enumeration.<br>

## Requirements

- curl
- jq
- nmap
- assetfinder
- dnstracer

## Installation

```bash
git clone https://github.com/blue0x1/Flora/
```
change the directory to Flora
```
cd Flora
```
change permissions 
``` bash
chmod +x flora
```
run it against target

``` bash 
./flora -d <target>
```
(optional: run it from anywhere) 

```
sudo cp flora /bin/
```

## Usage:
The basic usage of Flora is as follows: <br>
``` bash
flora -d <domain> [-m <mode>] [-w <wordlist>] [-v] [-s <shodan_api_key>] [-k <virustotal_api_key>] [-o <output_file>] [-X <securitytrails_api_key>] [-f] [-a]
```

## Options:
``` bash 
-d: The domain to scan.
-m: The mode of operation (discovery or takeover, default: discovery).
-w: The wordlist file to use for subdomain brute force (optional).
-v: Verbose mode for detailed output.
-t: The number of threads to use for subdomain brute force (default: 50).
-s: The Shodan API key (optional, use Shodan for subdomain enumeration).
-k: The VirusTotal API key (optional, use VirusTotal for subdomain enumeration).
-o: The output file path (optional, will output to console if not specified).
-f: Use fingerprinting to identify subdomains (default: false).
-a: Use Assetfinder for subdomain enumeration.
-X: The SecurityTrails API key (optional, use SecurityTrails for subdomain enumeration).
```
<br>
Note: It is recommended to obtain API keys for Shodan, VirusTotal, and SecurityTrails to increase the accuracy of subdomain enumeration.
