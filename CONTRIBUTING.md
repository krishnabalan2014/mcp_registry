# Contributing to MCP Registry

Thank you for your interest in contributing to the MCP Registry! This document provides guidelines for adding your MCP server to the registry.

## How to Add Your MCP Server

### 1. Fork the Repository

Fork this repository to your GitHub account by clicking the "Fork" button.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/mcp_registry.git
cd mcp_registry
```

### 3. Edit registry.json

Add your server entry to the `registry.json` file. Follow this schema:

```json
{
  "name": "io.github.username/server-name",
  "description": "Clear, concise description of what your MCP server does",
  "repository": "https://github.com/username/repository",
  "version": "1.0.0",
  "packages": [
    {
      "registry": "npm",
      "name": "your-package-name",
      "version": "1.0.0",
      "command": "npx",
      "arguments": [
        "your-package-name"
      ]
    }
  ]
}
```

### 4. Validate Your Entry

Ensure your JSON is valid:

```bash
# Using jq (install with: apt-get install jq or brew install jq)
jq . registry.json

# Or use an online validator
# https://jsonlint.com/
```

### 5. Test Locally (Optional)

Test your changes locally:

```bash
# Start a local web server
python3 -m http.server 8000

# Visit http://localhost:8000 in your browser
```

### 6. Commit Your Changes

```bash
git add registry.json
git commit -m "Add [your-server-name] to registry"
git push origin main
```

### 7. Create a Pull Request

1. Go to your fork on GitHub
2. Click "Pull Request"
3. Select the base repository and branch
4. Provide a clear description of your addition
5. Submit the pull request

## Server Entry Requirements

### Required Fields

- **name**: Unique identifier in reverse domain notation (e.g., `io.github.username/server-name`)
- **description**: Clear description of functionality (50-200 characters recommended)
- **repository**: Public GitHub repository URL

### Optional Fields

- **version**: Semantic version number
- **packages**: Array of package information
  - **registry**: Package registry type (`npm`, `pypi`, `oci`, etc.)
  - **name**: Package name
  - **version**: Package version
  - **command**: Command to run the package
  - **arguments**: Array of command arguments

## Guidelines

### Naming Convention

Use reverse domain notation for your server name:
- GitHub: `io.github.username/server-name`
- npm: `com.npmjs.package-name`
- Custom domain: `com.example.server-name`

### Description Best Practices

- Start with what the server does
- Keep it concise but informative
- Avoid marketing language
- Highlight key features or integrations

Example:
✅ Good: "Provides read and write access to Airtable databases with schema management"
❌ Bad: "The best, most amazing MCP server for Airtable!"

### Package Information

If your server is available through a package manager:
- Provide accurate version numbers
- Include all necessary installation arguments
- Document required environment variables (future enhancement)

## Code of Conduct

- Be respectful and professional
- Provide accurate information about your server
- Keep your entries up to date
- Don't add malicious or spam entries
- Respect intellectual property and licenses

## Questions or Issues?

- Open an issue for questions about the registry
- For MCP protocol questions, visit [modelcontextprotocol.io](https://modelcontextprotocol.io)
- Check existing entries for examples

## Review Process

Pull requests are reviewed by maintainers who will check:
- JSON validity
- Naming convention compliance
- Description clarity
- Link functionality
- No duplicate entries

Reviews typically happen within 1-3 business days.

## Updates and Maintenance

To update your existing entry:
1. Follow the same contribution process
2. Update the version number if applicable
3. Clearly describe changes in the PR

## License

By contributing to this registry, you agree that your contributions will be licensed under the same license as the project.

Thank you for contributing to the MCP ecosystem! 🚀
