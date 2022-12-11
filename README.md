# Installation (or run anytime to get latest version)
```bash
test -d ~/.ddev/commands/host && (cd ~/.ddev/commands/host && curl https://raw.githubusercontent.com/plumduffer/DDEV-Sitehost-Command/main/sitehost > sitehost && chmod +x sitehost)
```

Run `ddev poweroff` after install.

# How to use
Create a .env.sitehost in your DDEV app root (in the same directory as the .ddev directory) with the following environment variables set:

SITEHOST_SSH_IP=<br />
SITEHOST_SSH_USER=<br />
SITEHOST_SSH_PASSWORD=<br />
SITEHOST_DB_NAME=<br />
SITEHOST_DB_USER=<br />
SITEHOST_DB_PASSWORD=

You then have access to use the following commands:
- `ddev sitehost db` (clones the db from production and imports it into your DDEV)
- `ddev sitehost assets` (clones the ignored files from production's public folder into your DDEV public folder)
- `ddev sitehost ssh` (simply starts an ssh session on the site)
