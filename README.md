# Gnome Mail

A gnome-themed desktop client for chatting with locally installed Ollama models.
Messages appear as scrolls in an inbox and are saved in a local SQLite database.

This is a reviewed snapshot of the most recently updated source branch,
published as latest. Older branches and commit history are not included.

## Run

Install Python 3.10 or newer and Ollama, then download a local model with Ollama.
From this checkout:

    python3 -m venv .venv
    . .venv/bin/activate
    python -m pip install -r requirements.txt
    python run.py

On Windows, activate with .venv\Scripts\Activate.ps1 instead. The supplied
install.sh generates a Linux desktop shortcut; if you installed dependencies
in a virtual environment, set the shortcut's Exec command to that environment's
Python executable and this checkout's run.py.

The application uses the Ollama client's local default endpoint unless
OLLAMA_HOST overrides it. Choose a local model and keep the service on loopback.

## Privacy

Conversations, model names, responses, and error messages are stored unencrypted
under ~/.local/share/gnome-mail/messages.db. Keep that data and local credentials
out of Git. See [SECURITY.md](SECURITY.md) before sharing logs or changing endpoints.
