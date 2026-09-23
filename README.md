# Document Organiser

Windows AI document organiser for mixed client PDFs.

## Update channel

Installed copies use this repository as the official update source.

Manifest:
`https://raw.githubusercontent.com/universalbizcomply/fileorg/main/update/update_manifest.json`

Release assets are published under GitHub Releases. Existing installations use the in-app **Check for Updates** button; new installations use the full Windows installer.

## Persistent data

Application updates must never remove the user's:
- master SQLite client database
- continuous `clients_master.csv` mirror
- OpenAI credential stored in Windows Credential Manager
- NAPS2/OCR installation
- output documents
- settings

## Security

This repository is public. Never commit live client documents, API keys, passwords, authentication codes, UTRs, bank details, or customer databases.
