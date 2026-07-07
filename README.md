# MaLMon
Application of Machine Learning in Endpoint Monitor and Malware Classification system.

### Source code 
MaLMon Client: https://drive.google.com/drive/folders/1ebrzv9a0j6S8E5d1CfJJlO-BQ3txU13a?usp=drive_link

MaLMon Server: https://drive.google.com/drive/folders/18_RMAPVi6NFYSXGlAMuTru0DrJbBjThy?usp=drive_link

## Overview

This project develops a machine learning-based malware analysis framework capable of:

- Detecting & quanrantine malicious executable files
- Classifying malware types
- Leveraging the EMBER dataset for malware detection
- Utilizing MITRE ATT&CK incident reports for malware categorization and threat intelligence

---

## Features

- Binary Classification (Benign vs. Malicious)
- Malware Family Classification
- PE File Static Analysis
- Feature Engineering from EMBER Dataset
- ATT&CK Technique extraction with CAPA
- MITRE ATT&CK Intelligence Integration

## Workflow

<p align="center">
  <img
    src="https://raw.githubusercontent.com/Tuannq02/MaLMon/main/Workflow.png"
    alt="MaLMon System Architecture"
    width="900">
</p>

---

## Dataset & Tools

### EMBER Dataset

The project uses the EMBER (Endgame Malware Benchmark for Research) dataset, a large-scale benchmark dataset for Windows PE malware detection.

Dataset Repository:
https://github.com/elastic/ember

### MITRE ATT&CK

MITRE ATT&CK reports provide behavioral intelligence and malware technique mapping.

Website:
https://attack.mitre.org/

### CAPA
Detect capabilities in executable files.

Repository:
https://github.com/mandiant/capa

---

### Feature Extraction

Extracted features include:
- PE Header Information
- Section Metadata
- Imported Functions
- Exported Functions
- Byte Histograms
- String Features

### Malware Detection

Trained machine learning models to classify executable files as:
- Benign
- Malicious

### Malware Classification

Classify malicious files into malware categories such as:
- Trojan
- Ransomware
- Worm
- Spyware
- Adware
- Backdoor

---

## System Architecture

The proposed system follows a centralized malware analysis architecture consisting of:

### Central Server

The central server is responsible for:
- Receiving extracted static feature sets from endpoint clients
- Running malware detection and classification models
- Identifying malware families and threat categories
- Storing analysis results and logs

### Endpoint Client

A lightweight client is deployed on endpoint devices to:
- Monitor executable files
- Collect / Send file metadata
- Receive analysis results
- Performance migitation actions: quanrantine, removal or restore

<p align="center">
  <img
    src="https://raw.githubusercontent.com/Tuannq02/MaLMon/main/Client.png"
    alt="MaLMon System Architecture"
    width="700">
</p>

---

