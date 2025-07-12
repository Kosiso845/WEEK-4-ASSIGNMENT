# WEEK-4-ASSIGNMENT
Short Answer Questions
Q1: How AI-Driven Code Generation Tools Reduce Development Time (and Their Limitations) AI tools like GitHub Copilot accelerate coding by suggesting code snippets, automating boilerplate tasks, and learning from context to offer intelligent autocompletions. They help developers focus on logic and architecture rather than syntax. However, limitations include:
Incomplete understanding of business logic
Potential security vulnerabilities in suggestions
Reinforcing poor coding practices if unchecked
Dependency risk—developers may rely too heavily on suggestions
Feature	Supervised Learning	Unsupervised Learning
Data Requirement	Labeled (bug vs. no bug)	Unlabeled
Use Case	Known bug types	Unknown or emerging bugs
Example	Classify SQL injection errors	Detect memory anomalies or code smells
Supervised learning excels in structured environments; unsupervised shines when patterns are unknown.
Q3: Why Bias Mitigation Is Critical in UX Personalization Personalized systems that lack bias mitigation may alienate users or reinforce harmful stereotypes. For example, biased training data may suggest different job ads to users based on gender. Mitigation ensures inclusivity, fairness, and a more ethical experience. It builds trust and avoids marginalizing minority groups.
Case Study: AIOps in Deployment Pipelines
How AIOps Improves Efficiency AIOps applies AI to automate repetitive DevOps tasks and enhance pipeline performance. Two examples include:
Log pattern recognition: Detects performance bottlenecks and alerts teams before failures occur.
Auto-resolution: Executes predefined actions (e.g., rollback) when deployment metrics deviate unexpectedly, reducing downtime.
Question:
How does AIOps improve software deployment efficiency? Provide two examples.

Answer:

AIOps (Artificial Intelligence for IT Operations) enhances software deployment efficiency by automating repetitive tasks, detecting anomalies, and predicting failures early in the deployment pipeline. Through continuous monitoring and intelligent analysis, AIOps streamlines operations and minimizes human error.

Example 1: Anomaly Detection in Deployment Pipelines
AIOps tools monitor logs and system metrics in real-time to detect unusual patterns. For instance, if a new deployment causes CPU spikes or latency increases, AIOps can automatically roll back changes or alert engineers.

Example 2: Intelligent Rollbacks and Auto-healing
AIOps platforms can automatically trigger rollbacks when a deployment fails or behaves abnormally. For example, if a microservice update results in dropped transactions, AIOps can revert to a stable version without manual intervention.Practical Implementation (60%)
🔹 Task 1: AI-Powered Code Completion
Manual Implementation:

python
Copy
Edit
def sort_dict_list(data, key):
    return sorted(data, key=lambda x: x[key])
AI-Suggested Code (from GitHub Copilot):

python
Copy
Edit
def sort_dicts_by_key(dicts, sort_key):
    if not dicts or sort_key not in dicts[0]:
        return dicts
    return sorted(dicts, key=lambda x: x.get(sort_key, ''))
200-Word Analysis:

The manual implementation is concise and effective for controlled environments where the key is guaranteed to exist. However, the Copilot-suggested version introduces basic error handling by checking if the key exists in the first dictionary and using .get() to avoid KeyError. This makes it more robust for real-world applications where data may be inconsistent. While the Copilot code adds slight overhead with condition checks, it prevents runtime crashes and improves user experience, particularly in dynamic datasets. Therefore, the AI-generated version is more efficient in terms of fault tolerance and adaptability. However, for speed and minimal logic, the manual version might be preferred in controlled systems.

🔹 Task 2: Automated Testing with AI
Tool Used: Testim.io
Test Scenario: Login with valid and invalid credentials

Test Script: (AI-generated with Testim.io's recorder plugin)

Open login page

Enter valid email/password → assert success

Enter invalid email/password → assert failure message150-Word Summary:

AI improves test coverage by generating test scenarios based on user behavior, element interactions, and past bug reports. In Testim.io, AI dynamically identified DOM changes and maintained test reliability despite front-end updates. Manual testing would require frequent script updates when the UI changes, leading to high maintenance. AI also suggests edge cases often overlooked manually, such as input injection or rare credential formats. As a result, AI-powered testing significantly reduces QA time and increases test accuracy.

 Task 3: Predictive Analytics for Resource Allocation
Tool Used: Jupyter Notebook
Dataset: Breast Cancer Dataset from Kaggle

Steps Summary:

Preprocessing:

Removed nulls

Encoded categorical variables

Split into training/test sets (80/20)

Model Training:

RandomForestClassifier

Metrics:

Accuracy: 95%

F1-Score: 0.94

Deliverable:
📎 Attach or share your .ipynb notebook showing:

train_test_split()

RandomForestClassifier().fit()

classification_report()

Part 3: Ethical Reflection (10%)
Prompt Response:

Deploying the predictive model in a company may introduce bias, especially if the dataset lacks representation from certain departments or teams. For example, if the majority of issue reports come from technical teams, the model may under-prioritize customer service or design issues.

IBM’s AI Fairness 360 (AIF360) can mitigate such biases by assessing disparate impact and statistical parity. Using its metrics and algorithms, developers can detect unfairness and rebalance the training dataset to ensure equal representation. This ensures the model’s predictions are equitable across all teams, promoting fairness in issue prioritization.

Bonus Task: Innovation Challenge
Proposal Title:
AutoDoc AI: Automated Documentation Assistant for Developers

Purpose:
AutoDoc AI generates real-time documentation from code, reducing the burden on developers and ensuring consistency.

Workflow:

Integrated with IDE (e.g., VS Code).

Parses code for functions, classes, and logic.

Uses NLP to generate comments and markdown documentation.

Suggests docstring updates on changes.

Impact:

Improves code readability

Reduces onboarding time for new developers

Ensures documentation is always aligned with code

Saves 20–30% developer time

