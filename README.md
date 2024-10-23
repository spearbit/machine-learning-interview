# ML Engineer System Design Interview

## **System Design Task:**

You are tasked with designing and building a machine learning system that can detect malicious or vulnerable code inside a codebase. The system will be integrated into a GitHub repository and should be able to automatically detect potentially harmful code changes and flag them before they are pushed into production

You will have access to an internal dataset consisting of bugs and vulnerabilities (called _findings_) discovered in other repositories. These findings include the following information:

[code_files.json](code_files.json)

[findings_file_links.json](findings_file_links.json)

[findings_example.json](findings_example.json)

- The repository where the finding was found
- The file path
- The actual code of the file
- An explanation of the bug or vulnerability.
- The severity of the finding (low, medium, high, critical)

### Key Requirements:

- **GitHub Integration**: The system must be integrated with a GitHub repository and trigger on code changes (e.g., pull requests or commits). The specifics of how to integrate with GitHub will be up to you to figure out. Feel free to ask clarifying questions.
- **Training Data**: Use the internal _findings_ dataset to train a model capable of detecting potentially malicious or harmful code changes. You can use other data sources if deemed necessary
- **Model Performance**: The model should strike a balance between minimizing false positives and ensuring high recall, while giving feedback quickly enough to be useful during code review cycles.
- **Explainability**: The system must be able to provide a clear explanation of why certain lines of code were flagged as potentially harmful, so human reviewers can understand and verify the reasoning.
- **Evolving Threats**: The system should be able to adapt over time to new types of vulnerabilities and attack patterns. Consider how you would re-train or update the model to handle evolving threats.
- **Scalability**: The solution must scale to handle hundreds of repositories and potentially large codebases.

### Your Task:

- **Architecture**: Design a high-level architecture for this system, including key components such as data ingestion, model training, prediction, and feedback loops. Outline how you would structure the interaction with the GitHub repository, keeping performance and scalability in mind.
- **Modeling Approach**: Discuss the type of machine learning model(s) you would use. Would you leverage classical models, deep learning, or transformers? Explain your choice of model architecture, including how you would extract features from code, handle imbalanced datasets, and any other relevant preprocessing steps.
- **Trade-offs**: Consider the trade-offs between accuracy, performance, explainability, and scalability in your design. How would you minimize false positives while ensuring the model catches as much malicious code as possible?
- **Adaptation and Feedback**: Describe how the system could learn from new code submissions and adapt to new attack patterns over time. Would you implement online learning, periodic re-training, or another method to ensure the model evolves with new threats?
- **Security Considerations**: Since the system will operate in a security-critical context, discuss any additional security measures or best practices you would apply to ensure the model itself is not compromised or used maliciously.

During the discussion, we will dive into specific technical details, trade-offs, and any additional assumptions or design decisions you make.
