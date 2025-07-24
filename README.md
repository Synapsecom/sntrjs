# Automated Remote File Sync

This project maintains a local copy of a remote JavaScript asset.

## Purpose

Periodically checks for updates to an external script and syncs the latest version into this repository, ensuring the file remains current without manual intervention.

## How It Works

- A CI job runs on the `main` branch.
- It fetches a remote JavaScript file.
- If the file content has changed:
  - It commits the updated file.
  - Pushes the commit to the repository.

## CI/CD Requirements

- A GitLab Shell Runner.
- Two protected CI/CD variables:
  - `GITLAB_USER` — GitLab username or bot account.
  - `GITLAB_TOKEN` — Personal or project access token with `write_repository` scope.

## File Synced

- [`scout.js`](./scout.js): The auto-updated script.

## License

[MIT License](./LICENSE)
