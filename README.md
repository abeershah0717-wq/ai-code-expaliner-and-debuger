# 🧠 AI Code Explainer & Debugger

Paste your code and let Google Gemini **explain** it or **debug** it.
Built with pure Python, [Streamlit](https://streamlit.io) and the Gemini API.

## Features
- **Explain mode** – overview, step-by-step walkthrough, key concepts (Beginner / Intermediate / Advanced)
- **Debug mode** – finds bugs, explains tracebacks, returns fixed code
- Works with many languages (or auto-detect)
- Choose the Gemini model and temperature
- Download the result as Markdown

## Run locally

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

Get a free API key at <https://aistudio.google.com/apikey>, then either:

**Option A – paste the key in the app's sidebar**, or
**Option B – store it in a secrets file** (never commit it):

```toml
# .streamlit/secrets.toml
GEMINI_API_KEY = "your-key-here"
```

Start the app:

```bash
streamlit run app.py
```

## Deploy on Streamlit Community Cloud
1. Push this repo to GitHub.
2. Go to <https://share.streamlit.io> and sign in with GitHub.
3. Click **Create app** → select your repo, branch `main`, main file `app.py`.
4. Open **Advanced settings → Secrets** and add:
   ```toml
   GEMINI_API_KEY = "your-key-here"
   ```
5. Click **Deploy**.

## Project structure
```
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Privacy note
Code you submit is sent to Google's Gemini API. Do not paste passwords, API keys or confidential code.

## Changing models
Edit the `MODELS` list at the top of `app.py`. Available names are listed at
<https://ai.google.dev/gemini-api/docs/models>.

## License
MIT
