# MCP Registry

A centralized registry for Model Context Protocol (MCP) servers, hosted via GitHub Pages.

## 🌐 Live Registry

Access the registry at: **https://krishnabalan2014.github.io/mcp_registry/**

## 📋 What is This?

This repository provides a public registry endpoint for MCP servers, similar to an app store for Model Context Protocol implementations. The registry helps:

- **Client Applications**: Discover and integrate available MCP servers
- **Server Publishers**: Share their MCP servers with the community
- **Developers**: Browse the MCP ecosystem

## 🚀 Quick Start

### For Client Applications

Fetch the registry programmatically:

```javascript
fetch('https://krishnabalan2014.github.io/mcp_registry/registry.json')
  .then(response => response.json())
  .then(data => console.log(data));
```

### For Server Publishers

To add your MCP server to this registry:

1. Fork this repository
2. Edit `registry.json` and add your server details following the schema
3. Submit a pull request

#### Registry Schema

Each server entry should follow this format:

```json
{
  "name": "io.github.username/server-name",
  "description": "Brief description of your MCP server",
  "repository": "https://github.com/username/repo",
  "version": "1.0.0",
  "packages": [
    {
      "registry": "npm",
      "name": "package-name",
      "version": "1.0.0",
      "command": "npx",
      "arguments": ["package-name"]
    }
  ]
}
```

## 📁 Repository Structure

- `index.html` - Main registry web interface (GitHub Pages entry point)
- `registry.json` - JSON database of registered MCP servers

## 🔧 Setting Up GitHub Pages

To enable GitHub Pages for this repository:

1. Go to **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select branch: **main** (or your default branch)
4. Select folder: **/ (root)**
5. Click **Save**

GitHub will automatically deploy the site and make it available at your GitHub Pages URL.

## 📖 Learn More

- [Model Context Protocol Documentation](https://modelcontextprotocol.io)
- [Official MCP Registry](https://github.com/modelcontextprotocol/registry)

## 📄 License

This project is open source and available for public use.
