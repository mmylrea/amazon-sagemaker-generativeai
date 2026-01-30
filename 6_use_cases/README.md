# Use Cases

This directory contains real-world applications and industry-specific solutions demonstrating how to build production-ready Generative AI applications using Amazon SageMaker.

## 📚 Available Use Cases

### [RAG & Chatbots](usecases/rag_including_chatbot/)
Conversational AI with knowledge retrieval using FLAN-T5-XL and Falcon-7B models, featuring document processing and context-aware responses.

**Key Features:**
- Retrieval-Augmented Generation (RAG)
- Document ingestion and processing
- Context-aware question answering
- Production deployment patterns

### [Text Summarization](usecases/text_summarization/)
Document and content summarization using AI21, Falcon-7B, and FLAN-T5-XL models with LangChain integration.

**Key Features:**
- Multiple model options
- Extractive and abstractive summarization
- Batch processing capabilities
- LangChain integration

### [Text Summarization to Image](usecases/text_summarization_to_image/)
Multi-modal content generation pipeline combining text summarization with image generation capabilities.

**Key Features:**
- Text-to-summary pipeline
- Summary-to-image generation
- Multi-modal model integration
- Creative content generation

### [Text-to-SQL](usecases/text_to_sql/)
Natural language database querying using Code Llama with LangChain SQL query generation, complete with demo database and web interface.

**Key Features:**
- Natural language to SQL conversion
- Code Llama integration
- Interactive web interface
- Database connectivity examples

### [Phishing Detection](usecases/text_classification_for_phishing/)
Fine-tune Qwen2.5-1.5B for binary phishing detection using sequence classification on Amazon SageMaker AI.

**Key Features:**
- Fast inference (sub-second latency)
- Low cost deployment
- Production-ready implementation
- Comprehensive evaluation metrics
- See also: [Threat Intelligence Datasets](THREAT_INTELLIGENCE_DATASETS.md)

## 📊 Threat Intelligence Resources

### [Public Datasets for Threat Intelligence Training](THREAT_INTELLIGENCE_DATASETS.md)

A comprehensive guide to publicly available datasets for training machine learning models in cybersecurity and threat intelligence, including:

- **Phishing & Email Security**: PhishTank, APWG, Spam datasets
- **Malware Analysis**: EMBER, SOREL-20M, Malware Bazaar
- **Network Security**: CICIDS, NSL-KDD, UNSW-NB15
- **URL Intelligence**: URLhaus, malicious domain lists
- **Vulnerability Data**: NVD, Exploit-DB
- **Threat Actor Intelligence**: MITRE ATT&CK, AlienVault OTX

**Perfect for:**
- Security researchers building ML-based threat detection
- Data scientists exploring cybersecurity applications
- Organizations developing custom security solutions
- Students learning about ML in cybersecurity

[→ View Complete Threat Intelligence Datasets Guide](THREAT_INTELLIGENCE_DATASETS.md)

## 🎯 Getting Started

### Prerequisites
- AWS Account with SageMaker access
- Python 3.8+ environment
- Basic understanding of machine learning concepts
- Familiarity with the domain of your chosen use case

### Quick Start

1. **Choose a use case** that aligns with your needs
2. **Navigate to the use case directory** for detailed instructions
3. **Review the README** for prerequisites and setup steps
4. **Run the notebooks** in the specified order
5. **Customize and deploy** for your specific requirements

### General Workflow

```
Data Preparation → Model Training → Evaluation → Deployment → Monitoring
       ↓                 ↓             ↓           ↓            ↓
   S3 Storage    SageMaker Training   Metrics   Endpoints   CloudWatch
```

## 🛠️ Common Patterns

### Data Processing
- Load data from S3 or external sources
- Preprocess and format for model training
- Split into training/validation/test sets
- Upload processed data back to S3

### Model Training
- Configure SageMaker Training Jobs
- Use appropriate instance types (CPU/GPU)
- Monitor training with MLflow or CloudWatch
- Save model artifacts to S3

### Model Deployment
- Deploy to SageMaker Endpoints for real-time inference
- Use SageMaker Batch Transform for batch processing
- Configure auto-scaling for production workloads
- Implement A/B testing with traffic splitting

### Monitoring & Maintenance
- Track model performance metrics
- Monitor for data drift
- Implement automated retraining pipelines
- Set up alerts for anomalies

## 💡 Use Case Selection Guide

### For Text Understanding
✅ Use: RAG & Chatbots, Text Summarization  
✅ Models: FLAN-T5, Falcon, Llama  
✅ Instance: `ml.g5.xlarge` or larger

### For Code Generation
✅ Use: Text-to-SQL  
✅ Models: Code Llama, StarCoder  
✅ Instance: `ml.g5.2xlarge` recommended

### For Security Applications
✅ Use: Phishing Detection + [Threat Intelligence Datasets](THREAT_INTELLIGENCE_DATASETS.md)  
✅ Models: Qwen, BERT-based classifiers  
✅ Instance: `ml.g5.xlarge` for classification

### For Multi-Modal Applications
✅ Use: Text Summarization to Image  
✅ Models: Stable Diffusion, DALL-E  
✅ Instance: `ml.g5.2xlarge` or `ml.p3.2xlarge`

## 📖 Additional Resources

### Documentation
- [SageMaker Developer Guide](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html)
- [SageMaker Python SDK](https://sagemaker.readthedocs.io/)
- [Hugging Face on SageMaker](https://huggingface.co/docs/sagemaker/index)

### Related Sections
- [Getting Started](../1._getting_started/) - Setup and foundational concepts
- [Model Customization](../2_end_to_end_genai_on_sagemaker/2_model_customization/) - Fine-tuning techniques
- [Distributed Training](../3_distributed_training/) - Large-scale training
- [RAG Systems](../4_rag/) - Advanced retrieval patterns
- [AI Agents](../5_agents/) - Multi-agent systems
- [Inference Optimization](../7_inference/) - Performance tuning

### AWS Services
- [Amazon SageMaker](https://aws.amazon.com/sagemaker/)
- [Amazon Bedrock](https://aws.amazon.com/bedrock/)
- [AWS Lambda](https://aws.amazon.com/lambda/)
- [Amazon S3](https://aws.amazon.com/s3/)

## 🤝 Contributing

We welcome new use case contributions! Please ensure your submission includes:

1. **Complete implementation** - Working notebooks from data prep to deployment
2. **Documentation** - Clear README with prerequisites and instructions
3. **Code quality** - Well-commented, production-ready code
4. **Testing** - Validation of results and performance metrics
5. **Cost estimates** - Approximate AWS costs for running the example

See [CONTRIBUTING.md](../CONTRIBUTING.md) for detailed guidelines.

## 🆘 Support

- **Issues**: Report bugs or request features via GitHub Issues
- **Discussions**: Ask questions in GitHub Discussions
- **Documentation**: Check the main [README](../README.md) for comprehensive information

## 📄 License

This library is licensed under the MIT-0 License. See the [LICENSE](../LICENSE) file for details.

---

**Ready to build?** Choose a use case above and start developing your Generative AI application! 🚀
