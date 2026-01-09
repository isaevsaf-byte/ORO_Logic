# Deploying to Streamlit Community Cloud

## Quick Deploy Steps

1. **Push your code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Go to Streamlit Community Cloud**
   - Visit: https://share.streamlit.io/
   - Sign in with your GitHub account

3. **Deploy your app**
   - Click "New app"
   - Select your repository: `ORO_Logic`
   - Main file path: `app.py`
   - Click "Deploy"

4. **Your app will be live at:**
   `https://your-app-name.streamlit.app`

## Requirements

The `requirements.txt` file is already configured with:
- streamlit>=1.28.0
- pandas>=2.0.0
- openpyxl>=3.1.0

## Troubleshooting

If you encounter any errors:
1. Check the logs in Streamlit Cloud dashboard
2. Ensure all dependencies are in `requirements.txt`
3. Make sure `app.py` is in the root directory

