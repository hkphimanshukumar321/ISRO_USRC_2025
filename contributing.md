# Contributing to ANAV

Thank you for your interest in contributing to the ANAV project! We welcome contributions from developers, researchers, and enthusiasts who are passionate about advancing autonomous navigation and aerial robotics.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Reporting Issues](#reporting-issues)
3. [Feature Requests](#feature-requests)
4. [Pull Request Process](#pull-request-process)
5. [Coding Standards](#coding-standards)
6. [Commit Messages](#commit-messages)
7. [Additional Resources](#additional-resources)

---

## Getting Started

To contribute to ANAV, please follow these steps:

1. **Fork the Repository:**  
   Click the "Fork" button at the top right of the repository page to create your own copy.

2. **Clone Your Fork:**  
   Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-username/ANAV.git
   cd ANAV
Set Up Upstream Remote:
Configure the upstream remote to keep your fork updated:

bash
Copy
git remote add upstream https://github.com/original-author/ANAV.git
Create a New Branch:
Always create a new branch for your feature or bug fix:

bash
Copy
git checkout -b feature/your-feature-name
Reporting Issues
If you encounter bugs or have suggestions for improvement, please use the GitHub issue tracker:

Search for Existing Issues:
Check if your issue has already been reported to avoid duplicates.

Open a New Issue:
Provide a clear title and detailed description, including:

Steps to reproduce the issue
Expected and actual behavior
Environment details (e.g., OS, dependencies, etc.)
Feature Requests
We welcome ideas for new features! To propose a new feature:

Open an Issue:
Label it as "enhancement" or "feature".
Describe the Feature:
Include details on how the feature would work and its benefits.
Discuss and Collaborate:
Engage with maintainers and the community to refine the idea.
Pull Request Process
When you are ready to submit your changes, please follow these guidelines:

Branching:
Create a new branch for your work:
bash
Copy
git checkout -b feature/your-feature-name
Make Your Changes:
Commit your changes with clear, descriptive messages (see Commit Messages).
Ensure that your code adheres to the project’s coding standards.
Sync with Upstream:
Regularly update your branch with the latest changes from the upstream repository:
bash
Copy
git fetch upstream
git rebase upstream/main
Testing:
Run the existing tests and add new ones if your changes affect functionality.
Submit a Pull Request:
Push your branch to your fork:
bash
Copy
git push origin feature/your-feature-name
Open a pull request (PR) on GitHub and provide a clear description of your changes.
Follow any PR templates provided by the repository.
Coding Standards
To maintain a high-quality codebase, please adhere to the following standards:

Code Style:
Follow the existing style guidelines in the project. Use available linters and formatters.
Documentation:
Document your code, functions, and modules thoroughly.
Testing:
Include unit tests for new features and ensure existing tests pass.
Modularity:
Write modular and reusable code to ensure maintainability.
Commit Messages
Please write clear and concise commit messages. Use the following prefixes to indicate the nature of your change:

feat: for new features.
fix: for bug fixes.
docs: for documentation changes.
refactor: for code restructuring.
test: for adding or modifying tests.
chore: for maintenance or auxiliary changes.
Example:

sql
Copy
feat(navigation): add dynamic obstacle avoidance to SLAM module
Additional Resources
Code of Conduct: Please review our Code of Conduct to ensure a welcoming community.
Project Documentation: Refer to the docs/ directory for detailed project documentation.
Issue Tracker: Use the GitHub Issues page to report bugs or suggest improvements.
Thank you for contributing to ANAV! Your support and effort are essential to making this project successful.

Copy
