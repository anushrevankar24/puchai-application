# Puch AI MCP Server

This is an MCP (Model Context Protocol) server for Puch AI application process, optimized for fastmcp.cloud deployment.

## Features

- **Resume Tool**: Serves your resume in markdown format
- **Validation Tool**: Returns your phone number for verification  
- **Fetch Tool**: Fetches web content from URLs

## Quick Deploy to fastmcp.cloud

### 1. Deploy to fastmcp.cloud
1. Go to [fastmcp.cloud](https://fastmcp.cloud)
2. Connect your GitHub repository
3. Set environment variables:
   - `TOKEN`: `your_application_key_here`
   - `MY_NUMBER`: `your_phone_number_here`
   - `RESUME_FILE`: `resume.md`
4. Deploy!

### 2. Connect to Puch AI
Once deployed, use your fastmcp.cloud URL:
```
/mcp connect https://your-app.fastmcp.cloud/mcp your_application_key
```

## Local Development

### 1. Install Dependencies
```bash
pip install -r requirements.txt
```

### 2. Configure Environment
Create `.env` file:
```bash
TOKEN=your_application_key_here
MY_NUMBER=your_phone_number_here
HOST=0.0.0.0
PORT=8085
RESUME_FILE=resume.md
```

### 3. Run Server
```bash
python main.py
```

## Files

- `main.py` - Main MCP server code
- `resume.md` - Your resume in markdown format
- `requirements.txt` - Python dependencies
- `.env` - Environment configuration (for local development)

## Tools Available

1. **resume()** - Returns your resume as markdown
2. **validate()** - Returns your phone number
3. **fetch(url)** - Fetches content from URLs