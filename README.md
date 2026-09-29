# 📚 Snap & Study

A Streamlit chat app: enter your name and email once, then chat with an AI study
buddy by typing a question or attaching a photo of a problem, diagram, or page of
notes you're stuck on. Gemini explains the concept in plain language, and one
button emails a full recap of the conversation to you for later review.
Built with **Gemini** (chat + vision) and **Gmail SMTP** (free).

## Run locally
1. `python -m venv venv` and activate it
   (macOS/Linux: `source venv/bin/activate` · Windows: `.\venv\Scripts\Activate.ps1`)
2. `pip install -r requirements.txt`
3. Copy `.streamlit/secrets.toml.example` to `.streamlit/secrets.toml` and fill in:
   - Gemini API key (aistudio.google.com)
   - `GMAIL_ADDRESS` and a 16-char `GMAIL_APP_PASSWORD`
     (turn on 2-Step Verification, then myaccount.google.com/apppasswords)
4. `streamlit run app.py` -> http://localhost:8501

## Deploy
Push to GitHub (never commit `secrets.toml`), create an app at share.streamlit.io
with `app.py` as entry point, and paste your secrets under Settings -> Secrets.

## Files
- `app.py` - onboarding, chat, photo input, email send
- `prompts.py` - system prompt, welcome message, summary prompt
- `requirements.txt` - dependencies
