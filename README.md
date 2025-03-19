# AWS-Account-ID-Extractor-from-Access-Key-ID
This script extracts the AWS Account ID from a given AWS Access Key ID without requiring authentication. AWS Access Key IDs are Base32-encoded, and they contain embedded metadata, including the associated AWS Account ID. This script decodes the key and applies bitwise operations to reveal the 12-digit AWS Account ID.

# How It Works
Trims the first 4 characters of the Access Key ID (e.g., AKIA prefix).
Decodes the remaining characters using Base32 decoding.
Extracts the first 6 bytes from the decoded key.
Applies bitwise operations to filter the relevant bits.
Returns the AWS Account ID in a 12-digit format.

# Security Implications
This method can be used for reconnaissance in security assessments and red teaming.
Attackers can use leaked AWS Access Key IDs to identify target AWS accounts.
AWS does not officially document this technique, as it relies on reverse-engineering AWS key structures.

# Disclaimer
This script is intended for educational and security research purposes only. Misuse of this tool may violate AWS policies and terms of service. The author is not responsible for any unauthorized usage.
