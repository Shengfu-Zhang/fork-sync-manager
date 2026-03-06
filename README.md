# Fork Sync Manager

Automatically syncs all your GitHub forks with their upstream repos daily.

## Setup

1. Create a new repo on GitHub named `fork-sync-manager`
2. Push this repo to it
3. Create a PAT at https://github.com/settings/tokens with `repo` and `workflow` scopes
4. Add the PAT as a secret: repo Settings → Secrets → Actions → New secret → name it `PAT`
5. Edit `.github/workflows/sync.yml` and replace `REPLACE_WITH_YOUR_USERNAME` with your GitHub username
6. Add more forks to the matrix as needed

## Adding forks

Add entries to the matrix in `sync.yml`:

```yaml
- fork: your-username/repo-name
  upstream: original-org/repo-name
  branch: main
```
