## Spider

This Python script is a web crawler, or "spider," that recursively explores and collects all reachable URLs on a specified target website. The script is helpful for web penetration testers who need to map out the structure of a site or security researchers conducting reconnaissance.

### Features

- **Recursive Link Extraction**: The script follows links within a target URL, discovering and listing all reachable links.
- **URL Normalization**: Normalizes URLs by handling relative paths and removing fragments.

### How It Works

The script requests a webpage, extracts all URLs from the `href` attributes of anchor tags, and normalizes them to ensure they are fully-qualified URLs. It then recursively follows each discovered link that:
- Matches the target domain.
- Has not been visited already.

### Usage

1. **Set Target URL**
   - Update `target_url` with the website URL you wish to spider:
     ```python
     target_url = "http://***"
     ```

2. **Run the Script**
   - Use the following command:
     ```bash
     python spider.py
     ```

### Requirements

- **Python 3.x**
- **Requests Library**: Install using:
  ```bash
  pip install requests
  ```

### Example

For `target_url = "http://example.com"`, the output will list each discovered link within the domain:
```bash
http://example.com/page1
http://example.com/page2
http://example.com/page2/subpage
```

### Important Note

This script is intended for **use only on websites you have permission to test**. Unauthorized web crawling is illegal and can be unethical.

### Authors

- [Zaid Sabih](https://ie.linkedin.com/in/zaid-sabih-al-quraishi-5444a6127)
- [Uzoeshi Daniel](https://www.linkedin.com/in/daniel-ikenna-33b709235)
