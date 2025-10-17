# Notes

# GitHub Actions consist of:
- Workflows
- Jobs
- Steps

# Workflow Events
- Repository events
- Manual Trigger: from UI, API or another workflow
- Schedule

# Workflow runners
- GitHub-hosted Standard runners
- Windows
- Ubuntu
- Mac
## Why use them GitHub-Hosted runners
 - managed service
 - VM is scoped to a job
 - always run on a clean instance

## Self-hosted runners
- Any infastructure of your choice
- Full control
- Not managed
- Can be added at repo, org or enterprise level
- Job don't necessarily run on a clean instance
- do not use in self-hosted runner in public repos

# Actions
Custom applications to perform complex, frequently reapeated tasks.
- Avoids extensive and repetitive commands
- Prevents code duplication and reduces mistakes
- configured with key-value pair
- can be combined with other steps
- can create our own actions for public or private use
- Market place has public actions


