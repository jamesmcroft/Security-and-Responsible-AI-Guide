---
nav_order: 2
has_children: false
title: Chapter 1 - Understanding Security and Responsible AI
permalink: /chapters/chapter_01_understanding_security_and_responsible_ai
layout: default
---

# Chapter 1: Understanding Security and Responsible AI

Understanding the importance of security and responsible AI practices is the first step in establishing a strategy for implementing them. For organizations looking to build secure and responsible AI systems, this chapter provides an introduction to the concepts of building artificial intelligence into systems that are secure, robust, and ethical. Throughout the guide, we will build on the understanding in this chapter to provide guidance on how to design, implement, and monitor secure and responsible AI systems.

![Understanding Security and Responsible AI](../media/chapter_01.jpeg)

## Responsible AI Principles and Frameworks

Microsoft has established [a comprehensive standard for responsible AI](https://blogs.microsoft.com/wp-content/uploads/prod/sites/5/2022/06/Microsoft-Responsible-AI-Standard-v2-General-Requirements-3.pdf) which provides a framework for building AI systems that are built on six key principles.

- **Fairness**: AI systems should treat all people fairly. The data used should be diverse and representative of the population it is intended to serve. The system should be designed to avoid biased or discriminatory outcomes.
- **Reliability and safety**: AI systems should operate in a manner that is safe and reliable for all users. Data should be accurate, up-to-date, and validated. The system should be able to detect and mitigate against harmful outcomes.
- **Privacy and security**: AI systems should be designed to protect user data and maintain privacy. Data should be protected from unauthorized access, and the system should be designed to protect against malicious attacks.
- **Inclusiveness**: AI systems should empower everyone and engage people in both design and use. They should be designed to be accessible to all users regardless of their abilities, gender, ethnicity, age, or other characteristics.
- **Transparency**: AI systems should be designed to be understandable by anyone who interacts with them. The system should be able to explain its decision making process and provide information about how it works.
- **Accountability**: The people who design, build, and deploy AI systems should be accountable for how their systems operate. Human oversight should be built into the system to ensure that it upholds the principles of responsible AI.

The standard encourages collaboration and feedback at every step of the AI lifecycle, empowering customers, partners, researchers, and engineers to work together to build AI systems that are responsible.

By following the principles of the responsible AI standard, organizations can build AI systems that are secure and responsible while being flexible and adaptable to your use cases.

## Foundations of Security in AI on Azure

AI systems on Azure require a strong security foundation to ensure the confidentiality, integrity, and availability of data and models, as well as the resilience and trustworthiness of the system. Security in AI is not only a technical challenge, but also a business and ethical imperative. A security breach in an AI system can have severe consequences, such as data leakage, model theft, malicious manipulation, or denial of service.

To build secure AI systems on Azure, you need to follow the [Microsoft Zero Trust model](https://learn.microsoft.com/en-us/azure/well-architected/security/), which is based on the principle of verifying explicitly, using least-privilege access, and assuming breach. This model helps you to mitigate security risks by applying security controls at every layer of the system, from the data source to the model endpoint.

Best practices must be established to ensure that AI systems are designed and implemented with confidentiality, integrity, and availability in mind. You must consider:

- Defining a baseline security posture for your organization,
- Encrypting data at rest and in transit,
- Securing your data sources and pipelines, AI development and deployment environments, AI models and endpoints,
- Building monitoring and alerting into your AI systems,
- Establishing an incident response plan,
- Striving for continuous improvement of your practices in operationalizing AI systems.

Building secure AI systems on Azure requires a strong foundation of security practices. By establishing a baseline security posture for your organization, you can ensure that your AI systems are being designed and implemented with confidentiality, integrity, and availability in mind.
