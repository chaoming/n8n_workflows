# Contributing to n8n Workflows Collection

Thank you for your interest in contributing! This guide will help you add your workflows to this collection.

## 📋 Guidelines

### Workflow Quality Standards

1. **Tested**: Ensure your workflow has been tested and works as expected
2. **Documented**: Include clear descriptions and setup instructions
3. **Clean**: Remove any sensitive credentials or personal data
4. **Organized**: Place workflows in the appropriate category

### Workflow Naming Convention

- Use descriptive, kebab-case names: `slack-daily-summary.json`
- Include the main service/purpose in the name
- Keep names concise but meaningful

### Required Information

When submitting a workflow, include:

1. **Workflow Name**: Clear and descriptive
2. **Description**: What does this workflow do?
3. **Category**: Where does it belong? (productivity/social-media/data/notifications)
4. **Prerequisites**:
   - Required n8n version (if specific)
   - Required credentials/API keys
   - Third-party services needed
5. **Setup Instructions**: Step-by-step guide to configure the workflow
6. **Use Cases**: Example scenarios where this workflow is useful

### Adding Your Workflow

1. **Fork the Repository**
   ```bash
   git clone https://github.com/chaoming/n8n_workflows.git
   cd n8n_workflows
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b add-workflow-name
   ```

3. **Export Your Workflow from n8n**
   - Open your workflow in n8n
   - Click the menu (three dots) → Download
   - Save the `.json` file

4. **Add Documentation**
   - Create a `README.md` in the workflow's directory if needed
   - Or add an entry to the category's README

5. **Place the Workflow File**
   ```
   workflows/
   └── [category]/
       └── your-workflow-name.json
   ```

6. **Commit Your Changes**
   ```bash
   git add .
   git commit -m "Add: [Workflow Name] - [Brief Description]"
   ```

7. **Push and Create Pull Request**
   ```bash
   git push origin add-workflow-name
   ```

### Removing Sensitive Data

Before submitting, ensure you've removed:

- API keys and tokens
- Personal email addresses
- Private URLs and endpoints
- Database credentials
- Any other sensitive information

You can export workflows from n8n with credentials removed.

## 📝 Workflow Documentation Template

Create a `README.md` for your workflow if it's complex:

```markdown
# Workflow Name

## Description
Brief description of what this workflow does.

## Prerequisites
- n8n version: X.X.X or higher
- Required credentials: List all needed
- External services: Any APIs or services used

## Setup Instructions
1. Import the workflow into n8n
2. Configure credentials for [Service Name]
3. Set the following parameters:
   - Parameter 1: Description
   - Parameter 2: Description
4. Activate the workflow

## How It Works
Explain the workflow logic and key nodes.

## Use Cases
- Use case 1
- Use case 2

## Notes
Any additional information or tips.
```

## 🐛 Reporting Issues

If you find issues with existing workflows:

1. Check if the issue already exists
2. Provide detailed information:
   - Workflow name and version
   - n8n version
   - Error message or unexpected behavior
   - Steps to reproduce

## 💡 Suggestions

Have ideas for improving the repository structure or documentation? Open an issue with the "enhancement" label.

## 📜 Code of Conduct

- Be respectful and constructive
- Help others learn and improve
- Give credit where credit is due
- Follow the workflow quality standards

## ❓ Questions

If you have questions, feel free to:
- Open an issue with the "question" label
- Check existing issues and discussions
- Refer to the [n8n documentation](https://docs.n8n.io/)

Thank you for contributing! 🎉
