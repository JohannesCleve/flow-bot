# Flow Bot — releases

This repository only carries the release files for **Flow Bot**, die Keure's
internal desktop app for working with AI bots on Campus and ticket-flow's
flows. The source code lives elsewhere.

Installed copies poll the latest release here for `latest.json` and update
themselves. Each release holds:

- `latest.json` — the update manifest the app reads
- `flow-bot_<version>_aarch64.app.tar.gz` — the signed update
- `Flow Bot_<version>_arm64.dmg` — for a first install (Apple Silicon)

First install: open the dmg, drag Flow Bot to Applications, then run once in
Terminal:

```
xattr -cr "/Applications/Flow Bot.app"
```

Flow Bot needs Claude Code signed in with your Claude account (run `claude`
once), your repositories in `~/Sites`, and `az login` for Azure DevOps.
After that the app keeps itself current.
