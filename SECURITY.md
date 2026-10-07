# Security and conversation data

This is a personal desktop client, not a secure messaging service. It sends
prompts to the Ollama endpoint configured for your environment. Keep Ollama
on loopback, use local models, and review OLLAMA_HOST before sending private
information. A remote endpoint or cloud model can send your prompts outside
your device. The app does not add authentication or encryption to that service.

Model downloads and dependency installation require internet access. Using
already installed local models does not require internet or Bluetooth.

The local SQLite database stores conversations and errors in plain text.
Screenshots, backups, logs, and public issues can disclose those messages or
local paths. Do not commit databases, credentials, or private transcripts.
Dependency and model files should come from sources you trust.

Use GitHub private vulnerability reporting for security issues and redact
conversation contents, credentials, and device details from reports.
