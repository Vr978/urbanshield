# API Configuration Setup

## Setting up Mapbox API Token

Your Mapbox API token has been removed from the codebase for security. Here's how to configure it:

### Option 1: Using Environment Variables (Recommended)

1. Set the environment variable in your terminal:
```bash
export MAPBOX_API_TOKEN="your_actual_mapbox_token_here"
```

2. To make it permanent, add it to your shell configuration file:
   - For bash: Add to `~/.bashrc` or `~/.bash_profile`
   - For zsh: Add to `~/.zshrc`

### Option 2: Using a .env file

1. Create a `.env` file in the project root (already gitignored):
```bash
cp .env.example .env
```

2. Edit the `.env` file and add your actual Mapbox token

3. Install python-dotenv if not already installed:
```bash
pip install python-dotenv
```

4. Load the environment variables in your app (add to the top of `crime_files/app.py`):
```python
from dotenv import load_dotenv
load_dotenv()
```

## Getting a Mapbox Token

1. Go to [https://account.mapbox.com/](https://account.mapbox.com/)
2. Sign in or create an account
3. Navigate to "Access tokens"
4. Create a new token or copy an existing one

## Security Notes

⚠️ **Never commit API keys to version control**
- The `config_keys` file is now gitignored
- Use environment variables or `.env` files (also gitignored)
- The `.env.example` file shows the format without exposing secrets
