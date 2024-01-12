# Chapter 4: Implementing Security Measures

As AI becomes more prevalent in applications built on Azure, it is important to ensure that we continue to build them in a secure manner to protect against potential threats and vulnerabilities. This extends beyond the design of AI models and their use to include relevant security measures that can be implemented to protect the data, networks, and infrastructure that they rely on.

This chapter explores the best practices and guidance for implementing appropriate security measures for AI solutions built on Azure for both model development as well as solutions that leverage them.

![Implementing Security Measures](../media/chapter_04.jpg)

## Security best practices for building and deploying models with Azure Machine Learning

When building and deploying machine learning models on Azure, it is crucial to implement appropriate security measures to protect the end-to-end model development lifecycle. Microsoft's [security fundamentals for Azure](https://learn.microsoft.com/en-us/azure/security/fundamentals/zero-trust) provides a zero-trust security model that can be easily adapted to your machine learning solutions. The guiding principles stipulate that your machine learning solutions should be:

- **Verify explicitly**: Authenticate the identity of users or services requesting access to your Azure Machine Learning resources. Once authenticated, authorize by verifying permissions and access levels. Implementing both prevents unauthorized access to data and compute instances.
- **Use least privilege access**: Grant the minimum level of role-based access rights to users or services to perform their tasks in your Azure Machine Learning resources. When access is limited, the threat surface is reduced, and potential security risks are minimized.
- **Assume breach**: This principle is based on the idea that your Azure Machine Learning solution could be compromised at any time. Following this practice helps you to proactively guide design decisions, priorities, and operations to minimize the impact of a compromised AI solution.

To apply these principles in practice, you should consider the following best practices as outlined in Microsoft's [Azure Machine Learning security best practices](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/ai-machine-learning-enterprise-security):

- **Manage access to the Azure Machine Learning workspace and resources**: Use [Azure role-based access control](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-assign-roles?view=azureml-api-2&tabs=labeler) to define and enforce restrictions for users and services for your Azure Machine Learning workspace and its dependent resources, such as compute instances and data storage. Use built-in roles where possible, and custom roles if needed. Where possible, use a managed identity to allow access to other Azure resources from your Azure Machine Learning workspace to prevent exposing sensitive credentials.
- **Use Azure Key Vault to manage sensitive information**: When working with sensitive credentials, such as authentication keys for data sources, using [Azure Key Vault to store and manage](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-use-secrets-in-runs?view=azureml-api-2) them is recommended. A managed identity can be used to restrict access to the key vault from your Azure Machine Learning workspace.
- **Use a virtual network to isolate your Azure Machine Learning workspace**: To prevent unauthorized access to your Azure Machine Learning workspace, you should use a [managed virtual network to isolate it](https://learn.microsoft.com/en-us/azure/machine-learning/how-to-managed-network?view=azureml-api-2&tabs=azure-cli) to provide a secure environment to build and deploy machine learning models. Where necessary, you can use private endpoints to allow Azure services to access the network and can optionally define outbound rules to allow limited access to the internet.
- **Protect your model deployment endpoints**: When a model has been built, a model endpoint can be deployed to provide an API layer for your model to be consumed by other services within your AI solution. To protect your endpoints, you should always configure key or token-based authentication, and [disable public access using networking security](https://learn.microsoft.com/en-us/azure/machine-learning/concept-secure-online-endpoint?view=azureml-api-2&tabs=cli).

By following these security best practices for your machine learning solutions, you can build and deploy models on Azure with confidence.

## Maximizing security in LLM applications on Azure

## Conclusion
