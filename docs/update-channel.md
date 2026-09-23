# Document Organiser update channel

Installed builds read the manifest at:

`https://raw.githubusercontent.com/universalbizcomply/fileorg/main/update/update_manifest.json`

A release consists of:
- `DocumentOrganiserSetup.exe` for first-time installations
- `DocumentOrganiser_<version>_update.zip` for existing installations
- a SHA-256 checksum in `update/update_manifest.json`

Application updates replace only program files. Persistent data under `%APPDATA%\\DocumentOrganiser`, NAPS2/OCR, Windows Credential Manager secrets, and user output folders are preserved.

The repository is public. Never commit live client PDFs, credentials, client databases, authentication codes, tax identifiers, or other customer data.
