Automated Web Security Header & CORS Checker
Student: HibaPHarshad
Project category: Cybersecurity / Python
Program: IBM SkillsBuild Cyber Security 2026 (BharatCares)
Overview
This educational Python project checks a single authorized website for six common HTTP security headers and records a basic Cross-Origin Resource Sharing (CORS) response. It prints a report and saves the findings to scan_results.json.
Features
Validates that the input is a full HTTP/HTTPS URL.
Checks Strict-Transport-Security, Content-Security-Policy, X-Content-Type-Options, X-Frame-Options, Referrer-Policy, and Permissions-Policy.
Observes Access-Control-Allow-Origin and Access-Control-Allow-Credentials.
Reports HTTP status, final URL, errors, and a UTC timestamp.
Exports results as JSON.
Technologies
Python 3
Jupyter Notebook
requests library
HTTP response headers / basic CORS concepts
Files
HibaPHarshad_AutomatedWebScanner.ipynb — complete notebook code.
requirements.txt — required Python dependency.
HibaPHarshad_ProjectReport.docx — project documentation.
README.md — overview and run instructions.
Setup
Install Python 3.10 or later.
Open a terminal in this project folder.
(Optional but recommended) create and activate a virtual environment.
Install dependencies:
python -m pip install -r requirements.txt
Run
Open HibaPHarshad_AutomatedWebScanner.ipynb in Jupyter Notebook or JupyterLab.
Run the notebook cell.
Enter a URL for a website you own or have explicit permission to assess, for example a local test application or your organization's approved test site.
Review the printed report.
Find the generated scan_results.json in the current working directory.
Alternatively, copy the code cell into a .py file and run it with Python.
Interpreting results
Present: The response included the header.
Missing: The response did not include the header. Check whether it is appropriate for the application and configure it if needed.
CORS observation: The checker reports what the server returned for one test Origin. It does not prove that a CORS vulnerability exists.
Safety and ethical use
Use only systems you own or are explicitly authorized to test. The tool makes ordinary GET requests, does not exploit weaknesses, does not brute-force credentials, and does not crawl a site. Respect the site's terms and your organization's rules.
Limitations and future improvements
Checks only one URL at a time.
Does not inspect cookies, TLS configuration, JavaScript, authentication flows, or application logic.
Does not validate the full CORS policy or determine exploitability.
Future versions could add CSV/HTML reports, a GUI, configurable header profiles, and tests against a local deliberately vulnerable lab.