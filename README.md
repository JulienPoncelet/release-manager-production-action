# ReleaseManager Production Action

Automate production releases with versioning. Streamline deployments for efficient and controlled updates.

## Inputs

# TODO

## How to Obtain Inputs

1. **`github_token`**:
   - Go to your GitHub repository.
   - Navigate to Settings > Secrets.
   - Click on "New repository secret".
   - Add a secret named `GITHUB_TOKEN` and paste your GitHub token.

2. **`heroku_api_key`**:
   - Log in to your Heroku dashboard.
   - Navigate to Account settings > API Key.
   - Click on "Reveal" to show your API key.
   - Copy the API key.

3. **`slack_api_token` and `slack_channel_id`**:
   - Log in to your Slack workspace.
   - Navigate to Settings & administration > Manage apps.
   - Search for or create a new Slack app.
   - Go to the "OAuth & Permissions" section.
   - Copy the "Bot User OAuth Token" and "OAuth Access Token".
   - Invite the bot to the channel you want to post messages to.
   - Copy the ID of the channel you want to post messages to.

4. **`pat` (Personal Access Token)**:
   - Go to your GitHub account settings.
   - Navigate to Developer settings > Personal access tokens.
   - Click on "Generate new token".
   - Give your token a name and select the required scopes.
   - Click on "Generate token".
   - Copy the generated token.

## Usage

```yaml
- name: ReleaseManager Production
  uses: JulienPoncelet/release-manager-production-action@3.13.15
with:
	production_branch: master
	github_token: ${{ secrets.GITHUB_TOKEN }}
	heroku_api_key: ${{ secrets.HEROKU_API_KEY }}
	heroku_app_name: <Heroku App Name>
	slack_api_token: ${{ secrets.SLACK_API_TOKEN }}
	slack_channel_id: <Slack Channel ID>
	display_name: <Your Display Name>
	pat: ${{ secrets.PAT }}
```
