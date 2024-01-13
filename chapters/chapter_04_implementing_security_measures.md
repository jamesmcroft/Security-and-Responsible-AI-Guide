# Chapter 4: Implementing Security Measures

As AI becomes more prevalent in applications built on Azure, it is important to ensure that we continue to build them in a secure manner to protect against potential threats and vulnerabilities. This extends beyond the design of AI models and their use to include relevant security measures that can be implemented to protect the data, networks, and infrastructure that they rely on.

This chapter explores the best practices and guidance for implementing appropriate security measures for AI solutions built on Azure for both model development as well as solutions that leverage them.

![Implementing Security Measures](../media/chapter_04.jpg)

## Security best practices for building and deploying AI solutions on Azure

When building and deploying AI solutions on Azure, it is crucial to implement appropriate security measures to protect the end-to-end application lifecycle. Microsoft's [security fundamentals for Azure](https://learn.microsoft.com/en-us/azure/security/fundamentals/zero-trust) provides a zero-trust security model that can be easily adapted to your AI solutions. The guiding principles stipulate that your solution should be:

- **Verify explicitly**: Authenticate the identity of users or services requesting access to your Azure AI resources. Once authenticated, authorize by verifying permissions and access levels.
- **Use least privilege access**: Grant the minimum level of role-based access rights to users or services to perform their tasks in your Azure AI resources. When access is limited, the threat surface is reduced, and potential security risks are minimized.
- **Assume breach**: This principle is based on the idea that your Azure AI solution could be compromised at any time. Following this practice helps you to proactively guide design decisions, priorities, and operations to minimize the impact of a compromised AI solution.

### Applying best practices to secure your Azure Machine Learning solutions

To apply these principles in practice for Azure Machine Learning solutions, you should consider the following best practices as outlined in Microsoft's [Azure Machine Learning security best practices](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/ai-machine-learning-enterprise-security):

- **Manage access to the Azure Machine Learning workspace and resources**: Use [Azure role-based access control](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-assign-roles?view=azureml-api-2&tabs=labeler) to define and enforce restrictions for users and services for your Azure Machine Learning workspace and its dependent resources, such as compute instances and data storage. Use built-in roles where possible, and custom roles if needed. Where possible, use a managed identity to allow access to other Azure resources from your Azure Machine Learning workspace to prevent exposing sensitive credentials.
- **Use Azure Key Vault to manage sensitive information**: When working with sensitive credentials, such as authentication keys for data sources, using [Azure Key Vault to store and manage](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-use-secrets-in-runs?view=azureml-api-2) them is recommended. A managed identity can be used to restrict access to the key vault from your Azure Machine Learning workspace.
- **Use a virtual network to isolate your Azure Machine Learning workspace**: To prevent unauthorized access to your Azure Machine Learning workspace, you should use a [managed virtual network to isolate it](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-managed-network?view=azureml-api-2&tabs=azure-cli) to provide a secure environment to build and deploy machine learning models. Where necessary, you can use private endpoints to allow Azure services to access the network and can optionally define outbound rules to allow limited access to the internet.
- **Protect your model deployment endpoints**: When a model has been built, a model endpoint can be deployed to provide an API layer for your model to be consumed by other services within your AI solution. To protect your endpoints, you should always configure key or token-based authentication, and [disable public access using networking security](https://learn.microsoft.com/en-us/azure/machine-learning/concept-secure-online-endpoint?view=azureml-api-2&tabs=cli).

### Applying best practices to secure your Azure AI service solutions

When building and deploying AI solutions using Azure AI services, it is crucial to understand that traditional cybersecurity rules still apply when implementing security measures to protect your system from threats. Following the [Azure security baseline for Azure OpenAI](https://learn.microsoft.com/en-us/security/benchmark/azure/baselines/azure-openai-security-baseline), teams should consider the following practices in their solutions:

- **Use a managed identity to access Azure AI Services**: Use an [Azure Managed Identity](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/managed-identity) in combination with role-based access control to restrict access to your Azure AI services. This helps to prevent exposing API keys and ensures that only authorized services within your solution can access your AI services.
- **Choose a secure solution architecture**: When designing your AI solution, you should consider the [security of a well-architected solution](https://learn.microsoft.com/en-us/azure/well-architected/security/checklist) and how you can implement appropriate controls to mitigate against potential threats. [Integrating private access to your Azure OpenAI solution](https://techcommunity.microsoft.com/t5/fasttrack-for-azure/integrate-private-access-to-your-azure-open-ai-chatbot/ba-p/3994613) provides a useful guide on how to implement this for solutions taking advantage of Azure AI services.

### General best practices for ensuring security in AI solutions

In addition to the security specifics of Azure resources, it is important to also consider guidance that goes beyond the technical implementation of security measures. These include:

- **Training your team on security best practices**: It is important for everyone in your team to be aware of the risks and challenges that are posed by building AI solutions. Taking advantage of [Microsoft Defender for Cloud](https://azure.microsoft.com/en-us/products/defender-for-cloud/) can help to provide security recommendations and best practices for your team.
- **Keeping humans in the loop**: AI solutions should be designed to ensure that humans are always in the loop to make decisions and take action when necessary to prevent security breaches.
- **Proactively manage which decisions AI will be making**: The power of AI will provide your solutions with decision making processes that are potentially indeterminate. It is important to make well thought out choices as to what decisions AI will be making in your solution.
- **Stick to the basics**: Azure AI services and the models your build are fundamentally software, and teams should continue to employ existing cybersecurity, resilience, and secure-by-design principles.

## Conclusion

The increasing integration of AI into applications built on Azure requires teams to consider the critical importance of robust security measures. Beyond the technical implementation of security measures, teams should also consider the human and organizational aspects of security to ensure that they are building secure and trustworthy AI solutions.

By following the best practices and guidance outlined in this chapter, teams can ensure that they are building secure AI solutions that are resilient to potential threats and vulnerabilities. It is equally important for teams to continue to stay up to date with the evolving security landscape and implement appropriate controls to mitigate against them.
