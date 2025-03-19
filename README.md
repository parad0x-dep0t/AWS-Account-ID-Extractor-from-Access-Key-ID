# AWS-Account-ID-Extractor-from-Access-Key-ID
This script extracts the AWS Account ID from a given AWS Access Key ID without requiring authentication. AWS Access Key IDs are Base32-encoded, and they contain embedded metadata, including the associated AWS Account ID. This script decodes the key and applies bitwise operations to reveal the 12-digit AWS Account ID.


# How It Works
<br>Trims the first 4 characters of the Access Key ID (e.g., AKIA prefix).<br/>
<br>Decodes the remaining characters using Base32 decoding.<br/>
<br>Extracts the first 6 bytes from the decoded key.<br/>
<br>Applies bitwise operations to filter the relevant bits.<br/>
<br>Returns the AWS Account ID in a 12-digit format.<br/>

# Usage
Run the script and pass an AWS Access Key ID: python aws_account_extractor.py

# Security Implications
<br>This method can be used for reconnaissance in security assessments and red teaming.<br/>
<br>Attackers can use leaked AWS Access Key IDs to identify target AWS accounts.<br/>
<br>AWS does not officially document this technique, as it relies on reverse-engineering AWS key structures.<br/>


# Disclaimer
This script is intended for educational and security research purposes only. Misuse of this tool may violate AWS policies and terms of service. The author is not responsible for any unauthorized usage.
