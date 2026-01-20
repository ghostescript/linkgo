# linkgo
Find all links for multiple search queries.

`linkgo` is a Python-based command-line tool designed to discover and extract links from web pages. It leverages DuckDuckGo Search to find initial URLs based on a query, then delves into those pages to gather all outbound links.

## Features

- **DuckDuckGo Search Integration**: Utilizes DDGS to find relevant starting URLs for your queries.
- **Comprehensive Link Extraction**: Fetches web pages and parses their HTML content to extract all discoverable links.
- **Command-Line Interface**: Supports direct queries and output file specification via command-line arguments.
- **Interactive Mode**: Offers a user-friendly interactive prompt for dynamic searches.
- **Colorful Output**: Features an aesthetic gradient banner and colorized messages for better readability.

## **Linux Installation Only**
* Will work in Termux through any Linux Distro (Not ``proot-distro``)
### Install with PyPI 
```bash
pip install linkgo --break-system-packages
linkgo
```
### Clone the repository 
```bash
python -m venv venv 
source venv/bin/activate 
git clone https://github.com/ghostescript/linkgo
cd linkgo
pip install -r requirements.txt 
chmod +x linkgo.py
python linkgo.py
```
### Interactive Mode
```
┌──(kali㉿localhost)-[~]
└─$ linkgo

 /$$ /$$           /$$
| $$|__/          | $$
| $$ /$$ /$$$$$$$ | $$   /$$  /$$$$$$   /$$$$$$
| $$| $$| $$__  $$| $$  /$$/ /$$__  $$ /$$__  $$
| $$| $$| $$  \ $$| $$$$$$/ | $$  \ $$| $$  \ $$
| $$| $$| $$  | $$| $$_  $$ | $$  | $$| $$  | $$
| $$| $$| $$  | $$| $$ \  $$|  $$$$$$$|  $$$$$$/
|__/|__/|__/  |__/|__/  \__/ \____  $$ \______/
                             /$$  \ $$
                            |  $$$$$$/
                             \______/

   < https://github.com/ghostescript/linkgo >

Entering interactive mode...
Enter the search query (separated by spaces for multiple): github tools
Enter the output file to save links (or press Enter to print to console): git_tools.txt
Searching for 'github tools'...
Fetching and parsing links...

Links saved to git_tools.txt

Extracted 5129 unique links in 7.86 seconds for "github tools".
```
### Help Message 
```
┌──(kali㉿localhost)-[~]
└─$ linkgo -h
usage: linkgo [-h] [-o OUTPUT] query [query ...]

Find all links for multiple search queries.

positional arguments:
  query                The search query (can be multiple words
                       separated by spaces).

options:
  -h, --help           show this help message and exit
  -o, --output OUTPUT  Output file to save the links.
```
### Examples 
* Console Display 
```
linkgo github tools
```
* Save Scan to a File (Displays Fetching Errors Only)
```
linkgo github tools -o git_tools.txt
```

<br>

## Updated On 
``Jan 20, 2026``

<br>
