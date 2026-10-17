# ProblemFinder

An early Python prototype for collecting customer-interview files from Google Drive, intended to support later problem-theme analysis.

## Implemented

- OAuth-based Google Drive authentication
- Folder lookup by a configured path
- Downloading files whose names contain `interview`

The entry point is `src/main.py`; Drive operations are in `src/google_drive.py`.

## Not yet implemented

The NLP, text-processing, insight-generation, and utility modules are empty placeholders. The repository does not yet turn interviews into problem themes.

## Setup status

This is not a ready-to-run package. `requirements.txt` is empty, and OAuth configuration is not supplied. The source imports Google API Client and Google Auth OAuthlib packages and expects a local `credentials.json`; the empty placeholder under `config/` does not match that runtime path.

Before attempting a local run:

1. Define dependencies and a supported Python environment.
2. Review the Google Drive permission scope and configure OAuth for an account you control.
3. Update the folder path in `src/main.py`.
4. Keep credentials, cached tokens, and interview downloads outside version control.

## Privacy and scope

The current code requests broad Drive access and caches credentials locally. Customer interviews may contain confidential or personal information. Review access, storage, and consent requirements before collecting data.

