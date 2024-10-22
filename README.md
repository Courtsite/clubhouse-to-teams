# shortcut-to-teams

📝 A simple Google Cloud Function in Go to transform / proxy [Shortcut](https://shortcut.com/) (formerly, Clubhouse Project Management) webhooks to [Microsoft Teams](https://teams.microsoft.com/).

_This project is not feature complete, and it does not handle many cases. It has been tested with the Go 1.13 and 1.22 runtime._

![Notification in Teams](screenshot.png "Notification in Teams")

_Forked from https://github.com/Courtsite/clubhouse-to-discord_


## Getting Started

### Prerequisites

- Ensure you have `gcloud` installed:
    - MacOS: `brew cask install google-cloud-sdk`
    - Others: https://cloud.google.com/sdk/gcloud
- Ensure you have authenticated with Google Cloud: `gcloud init`
- (Optional) Set your current working project: `gcloud config set project <project>`

### Deployment

1. Clone / download a copy of this repository
2. Copy `.env.sample.yaml` to `.env.yaml`, and modify the environment variables declared in the file
3. Run `./deploy.sh`
4. Configure Shortcut webhooks integration in `https://app.shortcut.com/<workspace>/settings/integrations/outgoing-webhook`

![Shortcut's Generic Outgoing Webhook Integration](installation_1.png "Shortcut's Generic Outgoing Webhook Integration")

![Shortcut Generate API Token](installation_2.png "Shortcut Generate API Token")


## Migrating from Clubhouse to Shortcut

As of 2021-10-05, we have updated the function to reference "Shortcut" instead of the former "Clubhouse".

This updated function uses the latest Shortcut REST API specs. We suggest deploying this updated version, and updating your webhooks, before deleting the old `clubhouse-to-teams`.

If you do not update, your function may not work after November 13th, 2021.
