# AWS WAF Configuration Project

## Overview

This project focuses on configuring AWS Web Application Firewall (WAF) to protect against various types of attacks, including Distributed Denial of Service (DDoS), SQL Injection, Cross-Site Scripting (XSS), and other common web vulnerabilities. The project uses Terraform to provision and configure AWS WAF rules, rate-based rules, and web ACLs to enhance the security of web applications.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Files and Structure](#files-and-structure)
- [Implementation](#implementation)
  - [Main Configuration](#main-configuration)
  - [DDoS Protection](#ddos-protection)
  - [SQL Injection Protection](#sql-injection-protection)
  - [XSS Protection](#xss-protection)
  - [Generic Insecure Rules](#generic-insecure-rules)
  - [Bad IPs](#bad-ips)
  - [Regex Matching](#regex-matching)
- [Usage](#usage)
- [Conclusion](#conclusion)

## Prerequisites

- Terraform installed on your local machine.
- AWS account with necessary permissions to create and manage WAF resources.
- AWS CLI configured with appropriate access credentials.

## Files and Structure

The project consists of the following Terraform scripts:

1. `main.tf`: Main configuration file that initializes the AWS provider and manages resources.
2. `ddos.tf`: Configures rate-based rules to protect against DDoS attacks.
3. `sql_injection.tf`: Sets up rules to block SQL injection attacks.
4. `xss.tf`: Defines rules to mitigate XSS attacks.
5. `generic_insecure_rules_qs.tf`: Contains generic rules to block insecure patterns in query strings.
6. `bad_ips.tf`: Manages a list of known bad IP addresses to block.
7. `uri_regex.tf`: Implements URI-based regex matching rules.
8. `body_regex.tf`: Implements body-based regex matching rules.
9. `waf_acl.tf`: Configures the WAF ACL and associates it with the defined rules.
