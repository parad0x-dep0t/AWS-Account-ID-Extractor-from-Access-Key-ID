# AWS-Account-ID-Extractor-from-Access-Key-ID
This script extracts the AWS Account ID from a given AWS Access Key ID without requiring authentication. AWS Access Key IDs are Base32-encoded, and they contain embedded metadata, including the associated AWS Account ID. This script decodes the key and applies bitwise operations to reveal the 12-digit AWS Account ID.
