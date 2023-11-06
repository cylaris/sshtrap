# Cylaris SSHTrap
![GitHub last commit (by committer)](https://img.shields.io/github/last-commit/CyDefOps/project-killchain?style=flat-square&color=8A2BE2)
[![TI IOC Automation - FETCH](https://github.com/cylaris/sshtrap/actions/workflows/main.yml/badge.svg?branch=main)](https://github.com/cylaris/sshtrap/actions/workflows/main.yml)

## Threat Intelligence Feed

This repository is dedicated to providing a live feed of threat intelligence data, specifically Indicators of Compromise (IOCs), gathered from our SSH honeypot network. Our honeypot simulates SSH servers and records detailed information about attack patterns, which can be ingested directly into SIEM solutions for real-time security analysis.

## Honeypot Overview

Our SSH honeypot is built on top of robust open-source security projects and employs various levels of subterfuge to make it indistinguishable from a real SSH server. It captures and parses attack data, presenting clean and structured IOCs.

## IOCs and Data Structure

The IOCs provided here include:

- Timestamps
- Source IP Addresses
- Usernames and Passwords attempted
- SSHHASH
- SSH Client
- Status Returned by Honeypot

Data is structured in a JSON format, with fields corresponding to each type of IOC for easy parsing and ingestion by SIEM systems.

**Example IOC JSON structure:**

```
2023-11-03T12:00:30,43.243.74.20,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,345gs5662d34,345gs5662d34,failed
2023-11-03T12:00:32,43.243.74.20,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,root,3245gs5662d34,failed
2023-11-03T12:06:31,31.41.244.61,SSH-2.0-Go,4e066189c3bbeec38c99b1855113733a,crisam,123456,failed
2023-11-03T12:07:35,146.190.149.9,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,root,Litu@1234,failed
2023-11-03T12:07:36,146.190.149.9,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,root,3245gs5662d34,succeeded
2023-11-03T12:07:53,43.135.172.223,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,345gs5662d34,345gs5662d34,failed
2023-11-03T12:07:54,43.135.172.223,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,root,3245gs5662d34,succeeded
2023-11-03T12:08:12,129.226.208.154,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,345gs5662d34,345gs5662d34,failed
2023-11-03T12:08:15,129.226.208.154,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,root,3245gs5662d34,succeeded
2023-11-03T12:08:37,43.156.237.124,SSH-2.0-libssh_0.9.6,f555226df1963d1d3c09daf865abdc9a,345gs5662d34,345gs5662d34,failed
```

### Made with 🫶 by @[ntwrite](https://github.com/ntwrite) and @[KayaSEC](https://github.com/KayaSEC) 
