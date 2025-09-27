# 🚀 FastMCP.Cloud Deployment Guide

## Quick Deploy Steps

### 1. Push to GitHub
```bash
git init
git add .
git commit -m "Puch AI MCP Server"
git remote add origin https://github.com/yourusername/puch-ai-mcp.git
git push -u origin main
```

### 2. Deploy on fastmcp.cloud
1. Go to [fastmcp.cloud](https://fastmcp.cloud)
2. Click "Deploy New Server"
3. Connect your GitHub repository
4. Set environment variables in fastmcp.cloud dashboard:
   - `TOKEN`: `your_application_key_here`
   - `MY_NUMBER`: `your_phone_number_here`
   - `RESUME_FILE`: `resume.md`
5. Click "Deploy"

**🔒 Security Note:** Your .env file is NOT committed to GitHub (it's in .gitignore). 
Environment variables are set securely in the fastmcp.cloud dashboard.

### 3. Get Your Server URL
After deployment, you'll get a URL like:
`https://your-app.fastmcp.cloud`

### 4. Connect to Puch AI
Use this command in Puch:
```
/mcp connect https://your-app.fastmcp.cloud/mcp your_application_key
```

## Environment Variables for fastmcp.cloud

| Variable | Value | Description |
|----------|-------|-------------|
| `TOKEN` | `your_application_key_here` | Your Puch AI application key |
| `MY_NUMBER` | `your_phone_number_here` | Your phone number for validation |
| `RESUME_FILE` | `resume.md` | Path to your resume file |

## Files Included

- ✅ `main.py` - MCP server code
- ✅ `resume.md` - Your formatted resume
- ✅ `requirements.txt` - Python dependencies
- ✅ `README.md` - Documentation

## Testing Your Deployment

Once deployed, test your server:
```bash
curl https://your-app.fastmcp.cloud/mcp
```

You should get a 401 Unauthorized response (this is correct - it means your server is running and secured).

## Ready for Puch AI! 🎉