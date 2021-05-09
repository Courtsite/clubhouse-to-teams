# clubhouse-to-teams

📝 A simple Google Cloud Function in Go to transform / proxy [Clubhouse](https://clubhouse.io/) (Project Management) webhooks to [Microsoft Teams](https://teams.microsoft.com/).

_This project is still under development, and it does not handle many cases. It has been tested with the Go 1.13 runtime._

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
4. Configure Clubhouse webhooks integration in `https://app.clubhouse.io/<workspace>/settings/integrations/outgoing-webhook`

![Clubhouse's Generic Outgoing Webhook Integration](installation_1.png "Clubhouse's Generic Outgoing Webhook Integration")

![Clubhouse Generate API Token](installation_2.png "Clubhouse Generate API Token")
