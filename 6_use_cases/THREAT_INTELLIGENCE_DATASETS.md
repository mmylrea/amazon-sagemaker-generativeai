# Public Datasets for Threat Intelligence Training

This document provides a comprehensive list of publicly available datasets that can be used for training machine learning models for threat intelligence, security analysis, and cybersecurity applications on Amazon SageMaker.

## 📊 Overview

The datasets listed below cover various aspects of threat intelligence including:
- Phishing and malicious email detection
- Malware analysis and classification
- Network intrusion detection
- URL and domain reputation
- Threat actor behavior analysis
- Vulnerability intelligence

## 🔒 Phishing and Email Security

### 1. Phishing Emails Dataset
- **Source**: [HuggingFace - drorrabin/phishing_emails-data](https://huggingface.co/datasets/drorrabin/phishing_emails-data)
- **Original**: [Kaggle - Phishing Emails](https://www.kaggle.com/datasets/subhajournal/phishingemails)
- **Size**: ~27,000 training samples, ~3,700 test samples
- **Format**: Text (email content) with binary labels (safe/phishing)
- **Use Case**: Binary classification for phishing detection
- **Example Implementation**: See [Phishing Detection with Sequence Classification](usecases/text_classification_for_phishing/)

### 2. APWG eCrime Dataset
- **Source**: [Anti-Phishing Working Group (APWG)](https://apwg.org/trendsreports/)
- **Type**: Phishing URLs, phishing site screenshots
- **Update Frequency**: Quarterly reports
- **Use Case**: Phishing URL detection, trend analysis
- **Access**: Free with registration

### 3. PhishTank
- **Source**: [PhishTank Database](https://www.phishtank.com/developer_info.php)
- **Type**: Community-verified phishing URLs
- **Format**: JSON/CSV exports available
- **Update Frequency**: Real-time, updated hourly
- **Use Case**: URL reputation, phishing detection training
- **License**: Free for non-commercial use

### 4. Email Security Dataset (SPAM/HAM)
- **Source**: [SpamAssassin Public Corpus](https://spamassassin.apache.org/old/publiccorpus/)
- **Size**: Multiple corpora with thousands of emails
- **Format**: Raw email text
- **Use Case**: Spam detection, email filtering
- **License**: Apache License

## 🦠 Malware Analysis

### 5. EMBER (Endgame Malware BEnchmark for Research)
- **Source**: [EMBER Dataset](https://github.com/elastic/ember)
- **Size**: 1.1 million PE files (900K training, 200K testing)
- **Format**: Extracted features and raw PE files
- **Use Case**: Malware detection, binary classification
- **Labels**: Malicious, benign, unlabeled
- **Year**: 2018 dataset, widely used benchmark

### 6. SOREL-20M
- **Source**: [Sophos-ReversingLabs Malware Dataset](https://github.com/sophos/SOREL-20M)
- **Size**: 20 million PE files
- **Format**: Pre-extracted features, metadata, and disassembly
- **Use Case**: Large-scale malware detection, deep learning
- **License**: Creative Commons (with restrictions)

### 7. Malware Bazaar
- **Source**: [abuse.ch Malware Bazaar](https://bazaar.abuse.ch/)
- **Type**: Recent malware samples
- **Format**: Malware binaries, YARA rules
- **Update Frequency**: Daily updates
- **Use Case**: Malware analysis, signature generation
- **Access**: Free API available

### 8. VirusTotal
- **Source**: [VirusTotal API](https://www.virustotal.com/gui/home/upload)
- **Type**: File hashes, detection results from 70+ antivirus engines
- **Format**: API responses (JSON)
- **Use Case**: Malware classification, threat intelligence
- **Access**: Free tier available (limited requests)

## 🌐 Network Security and Intrusion Detection

### 9. CICIDS 2017/2018 (Canadian Institute for Cybersecurity)
- **Source**: [CIC-IDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)
- **Size**: ~2.8 million network flows
- **Format**: CSV with 80+ features
- **Attack Types**: Brute Force, DoS, DDoS, Web Attack, Infiltration, Botnet
- **Use Case**: Network intrusion detection, anomaly detection
- **Labels**: Normal and 14 attack categories

### 10. NSL-KDD Dataset
- **Source**: [NSL-KDD](https://www.unb.ca/cic/datasets/nsl.html)
- **Type**: Improved version of KDD Cup 99
- **Size**: 125,973 training records, 22,544 test records
- **Format**: CSV with 41 features
- **Use Case**: Network intrusion detection benchmarking
- **Labels**: Normal, DoS, Probe, R2L, U2R

### 11. UNSW-NB15 Dataset
- **Source**: [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
- **Size**: 2.5 million records
- **Format**: CSV with 49 features
- **Attack Types**: 9 attack categories (Fuzzers, Analysis, Backdoors, DoS, Exploits, Generic, Reconnaissance, Shellcode, Worms)
- **Use Case**: Network traffic analysis, intrusion detection

### 12. CTU-13 Botnet Dataset
- **Source**: [CTU-13 Dataset](https://www.stratosphereips.org/datasets-ctu13)
- **Type**: Real botnet traffic captures
- **Size**: 13 different botnet scenarios
- **Format**: PCAP files, NetFlow
- **Use Case**: Botnet detection, C&C communication analysis

## 🔗 URL and Domain Intelligence

### 13. URLhaus
- **Source**: [URLhaus by abuse.ch](https://urlhaus.abuse.ch/)
- **Type**: Malicious URLs distributing malware
- **Format**: CSV/JSON exports
- **Update Frequency**: Real-time updates
- **Use Case**: URL reputation, malware distribution detection
- **Access**: Free API and bulk downloads

### 14. Alexa Top 1M / Majestic Million
- **Source**: [Majestic Million](https://majestic.com/reports/majestic-million)
- **Type**: Top legitimate domains (for negative samples)
- **Format**: CSV
- **Update Frequency**: Daily
- **Use Case**: Training benign domain samples for URL classifiers

### 15. MalwareURL Dataset
- **Source**: [MalwareURL](https://www.malwareurl.com/)
- **Type**: URLs hosting malware
- **Format**: Text lists
- **Use Case**: URL filtering, threat intelligence feeds

## 🎯 Exploit and Vulnerability Intelligence

### 16. Exploit Database
- **Source**: [Exploit-DB](https://www.exploit-db.com/)
- **Type**: Publicly disclosed exploits and vulnerabilities
- **Format**: Text, code samples, descriptions
- **Use Case**: Vulnerability analysis, exploit detection
- **Access**: Free browsing, searchable database

### 17. NVD (National Vulnerability Database)
- **Source**: [NVD](https://nvd.nist.gov/)
- **Type**: CVE database with CVSS scores
- **Format**: JSON feeds, API
- **Use Case**: Vulnerability prioritization, risk assessment
- **Update Frequency**: Continuous

### 18. VulnDB
- **Source**: [VulnDB by Risk Based Security](https://vulndb.cyberriskanalytics.com/)
- **Type**: Vulnerability intelligence
- **Format**: API access
- **Use Case**: Comprehensive vulnerability tracking
- **Access**: Free tier available

## 🕵️ Threat Actor and IOC Intelligence

### 19. MITRE ATT&CK
- **Source**: [MITRE ATT&CK Framework](https://attack.mitre.org/)
- **Type**: Adversary tactics, techniques, and procedures (TTPs)
- **Format**: JSON, STIX
- **Use Case**: Threat hunting, behavioral analysis, defensive strategy
- **Coverage**: Enterprise, Mobile, ICS environments

### 20. AlienVault OTX (Open Threat Exchange)
- **Source**: [AlienVault OTX](https://otx.alienvault.com/)
- **Type**: Community threat intelligence platform
- **Format**: API access to IOCs, pulses
- **Use Case**: Real-time threat intelligence feeds
- **Access**: Free with registration

### 21. Abuse.ch Threat Intel Feeds
- **Source**: [abuse.ch](https://abuse.ch/)
- **Feeds**: 
  - Feodo Tracker (botnet C&Cs)
  - SSL Blacklist (malicious SSL certificates)
  - URLhaus (malware URLs)
- **Format**: CSV, JSON, various formats
- **Update Frequency**: Real-time
- **Use Case**: IOC feeds, threat detection

## 📱 Mobile Security

### 22. AndroZoo
- **Source**: [AndroZoo](https://androzoo.uni.lu/)
- **Size**: Millions of Android APKs
- **Format**: APK files with VirusTotal scan results
- **Use Case**: Android malware detection
- **Access**: Academic/research access with approval

### 23. Drebin Dataset
- **Source**: [Drebin](https://www.sec.cs.tu-bs.de/~danarp/drebin/)
- **Size**: 129,013 applications (5,560 malware)
- **Format**: Extracted features
- **Use Case**: Android malware classification
- **Year**: 2014, widely cited benchmark

## 🌍 Darknet and Underground Markets

### 24. DARPA Intrusion Detection Dataset
- **Source**: Various research archives
- **Type**: Network traffic with labeled attacks
- **Use Case**: Historical benchmark, comparison studies
- **Note**: Older dataset but useful for baseline comparisons

### 25. Tor Exit Node Lists
- **Source**: [Tor Metrics](https://metrics.torproject.org/)
- **Type**: Public Tor exit nodes
- **Use Case**: Anonymization detection, traffic analysis
- **Update Frequency**: Real-time

## 🔬 Specialized Security Datasets

### 26. DNS Tunnel Dataset
- **Source**: Various research papers and GitHub repositories
- **Type**: DNS query patterns for tunneling detection
- **Use Case**: Covert channel detection

### 27. Ransomware Dataset
- **Source**: [No More Ransom](https://www.nomoreransom.org/)
- **Type**: Ransomware samples and decryption tools
- **Use Case**: Ransomware detection and classification

### 28. IoT Security Dataset
- **Source**: [IoT-23 Dataset](https://www.stratosphereips.org/datasets-iot23)
- **Type**: Network traffic from IoT devices (malicious and benign)
- **Format**: PCAP, labeled flows
- **Use Case**: IoT threat detection

## 🛠️ Using These Datasets with Amazon SageMaker

### Data Preparation
```python
import boto3
import sagemaker
from datasets import load_dataset

# Example: Loading HuggingFace dataset and uploading to S3
dataset = load_dataset("drorrabin/phishing_emails-data")
s3_client = boto3.client('s3')
bucket = sagemaker.Session().default_bucket()

# Process and upload
# See: 6_use_cases/usecases/text_classification_for_phishing/
```

### Training Approaches

1. **Supervised Learning**
   - Binary classification (malicious/benign)
   - Multi-class classification (attack types)
   - Sequence classification for text-based threats

2. **Unsupervised Learning**
   - Anomaly detection for zero-day threats
   - Clustering for threat grouping
   - Dimensionality reduction for feature engineering

3. **Transfer Learning**
   - Fine-tune foundation models (Llama, Qwen, etc.)
   - Use pre-trained embeddings
   - Domain adaptation techniques

### Recommended SageMaker Features

- **SageMaker Training Jobs**: Distributed training for large datasets
- **SageMaker Endpoints**: Real-time threat detection
- **SageMaker Batch Transform**: Bulk analysis of threat data
- **SageMaker Pipelines**: Automated retraining with new threat data
- **SageMaker Model Monitor**: Track model performance against evolving threats

## 📋 Dataset Selection Guidelines

### For Phishing Detection
✅ Use: PhishTank, APWG, Phishing Emails Dataset  
✅ Model: Text classification (BERT, RoBERTa, Qwen)  
✅ Instance: `ml.g5.xlarge` or `ml.g5.2xlarge`

### For Malware Classification
✅ Use: EMBER, SOREL-20M, Malware Bazaar  
✅ Model: Gradient boosting (XGBoost), neural networks  
✅ Instance: `ml.m5.xlarge` for features, `ml.p3.2xlarge` for raw binaries

### For Network Intrusion Detection
✅ Use: CICIDS 2017/2018, UNSW-NB15, NSL-KDD  
✅ Model: Random Forest, LSTM, GNN  
✅ Instance: `ml.m5.4xlarge` or `ml.c5.4xlarge`

### For URL Reputation
✅ Use: URLhaus, PhishTank, Alexa/Majestic  
✅ Model: Character-level CNN, BERT for URLs  
✅ Instance: `ml.g5.xlarge`

## ⚠️ Important Considerations

### Legal and Ethical
- **Terms of Service**: Always review dataset licenses
- **Research Use**: Many datasets are for research/academic use only
- **Data Privacy**: Be cautious with datasets containing PII
- **Responsible Disclosure**: Don't use malware samples maliciously

### Data Quality
- **Label Accuracy**: Community-labeled data may have errors
- **Class Imbalance**: Many security datasets are heavily imbalanced
- **Temporal Drift**: Threats evolve; retrain models regularly
- **False Positives**: Security models need careful threshold tuning

### Best Practices
1. **Split data properly**: Time-based splits for temporal datasets
2. **Monitor performance**: Use SageMaker Model Monitor
3. **Version control**: Track datasets and model versions
4. **Adversarial testing**: Test against evasion techniques
5. **Explainability**: Use SHAP/LIME for security decision explanations

## 🔗 Additional Resources

### Research Papers
- [A Survey of Machine Learning for Cybersecurity](https://dl.acm.org/doi/10.1145/3450288)
- [Adversarial Machine Learning in Cybersecurity](https://arxiv.org/abs/1804.09470)

### AWS Security Services
- [Amazon GuardDuty](https://aws.amazon.com/guardduty/) - Threat detection service
- [AWS Security Hub](https://aws.amazon.com/security-hub/) - Security posture management
- [Amazon Macie](https://aws.amazon.com/macie/) - Data security and privacy

### Related Examples
- [Phishing Detection Example](usecases/text_classification_for_phishing/) - End-to-end implementation
- [SageMaker Security Best Practices](https://docs.aws.amazon.com/sagemaker/latest/dg/security.html)

## 📬 Contributing

Have a dataset to add? Please submit a pull request with:
- Dataset name and source
- Size and format details
- Typical use cases
- License information
- Example code (if available)

---

**Last Updated**: January 2026  
**Maintained By**: AWS Samples Community

For questions or issues, please open a GitHub issue in this repository.
