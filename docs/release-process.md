# Publishing a Document Organiser update

The in-app updater is already pointed at this repository.

## Build on the Windows release machine

1. Update `VERSION.txt`, `src/version.py`, and the installer version.
2. Run `Build_Distributable_Installer.bat`.
3. The build creates:
   - `installer_output/DocumentOrganiserSetup.exe`
   - `update_output/DocumentOrganiser_<version>_update.zip`
   - `update_output/update_manifest.json`

## Publish

1. Create a GitHub Release named/tagged `v<version>`.
2. Upload the installer and update ZIP.
3. Verify the release asset URL matches the `package_url` in the generated manifest.
4. Replace `update/update_manifest.json` on `main` with the generated manifest only after the release assets are available.

Installed copies will then see the new version through **Check for Updates**.

## Safety rule

Never publish a manifest for a version until its update ZIP exists and its SHA-256 checksum has been verified. Never upload client documents, client databases, OpenAI keys, authentication codes, tax identifiers, or other customer data to this public repository.
