# Action Repository for Testing GitHub Webhooks

This repository is used to test GitHub webhook events for the webhook dashboard application.

## Purpose
This repository generates the following GitHub events:
- **Push events** - When commits are pushed to branches
- **Pull request events** - When PRs are opened
- **Merge events** - When PRs are merged

## Test Files
- `test-files/sample.txt` - For testing push events
- `test-files/feature.md` - For testing pull request events
- `test-files/config.json` - Configuration file for testing

## Webhook Configuration
This repository is configured to send webhooks to the GitHub Webhook Dashboard application.

## Testing Instructions

### Test Push Events
```bash
echo "Update $(date)" >> test-files/sample.txt
git add .
git commit -m "Test push event"
git push origin main
