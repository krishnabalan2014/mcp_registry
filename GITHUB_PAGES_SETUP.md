# GitHub Pages Setup Instructions

## Prerequisites
- Repository must be public (or have GitHub Pro/Enterprise for private repos)
- You must have admin access to the repository

## Steps to Enable GitHub Pages

1. **Navigate to Repository Settings**
   - Go to your repository on GitHub
   - Click on "Settings" tab

2. **Go to Pages Section**
   - In the left sidebar, click on "Pages"

3. **Configure Source**
   - Under "Build and deployment"
   - Select "Deploy from a branch"
   - Choose your branch (e.g., `main` or `copilot/create-index-html-for-mcp`)
   - Select folder: `/ (root)`
   - Click "Save"

4. **Wait for Deployment**
   - GitHub will automatically build and deploy your site
   - This usually takes 1-2 minutes
   - You'll see a green checkmark when it's ready

5. **Access Your Site**
   - Your site will be available at:
   - `https://krishnabalan2014.github.io/mcp_registry/`

## Verifying the Deployment

Once deployed, you can verify:

1. **Main Page**: Visit `https://krishnabalan2014.github.io/mcp_registry/`
2. **JSON Endpoint**: Visit `https://krishnabalan2014.github.io/mcp_registry/registry.json`

## Troubleshooting

### Site Not Loading
- Check that GitHub Pages is enabled in Settings
- Verify the branch and folder are correct
- Wait a few minutes for the initial deployment

### 404 Error
- Ensure `index.html` is in the root of your selected branch
- Check that the branch is up to date

### JSON Not Loading
- Verify `registry.json` exists in the repository
- Check browser console for any errors
- Ensure the file has valid JSON syntax

## Updating the Registry

After initial setup, any push to the configured branch will automatically trigger a new deployment:

```bash
# Make changes to registry.json or index.html
git add .
git commit -m "Update registry"
git push
```

The site will update within 1-2 minutes.

## Custom Domain (Optional)

If you want to use a custom domain:

1. Go to Settings → Pages
2. Enter your custom domain under "Custom domain"
3. Configure DNS records with your domain provider
4. Follow GitHub's instructions for DNS verification

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Model Context Protocol](https://modelcontextprotocol.io)
