## Main repos backup

Manual incremental update:

- Install [`github-backup`](https://pypi.org/project/github-backup/). Like `pipx install github-backup`.

- Create a fine-grained personal access token for `nvim-mini/mini.nvim` and `nvim-mini/MiniMax` repos with at least these **read-only** permissions: `issues`, `pull-requests`, `discussions`, `metadata`. Save it locally and make sure it is available as `$GH_MINI_BACKUP` environment variable.

- Run from the repo root:

    ```bash
    github-backup nvim-mini -f $GH_MINI_BACKUP -R mini.nvim --incremental --issues --issue-comments --pulls --pull-comments --labels --discussions

    github-backup nvim-mini -f $GH_MINI_BACKUP -R MiniMax --incremental --issues --issue-comments --pulls --pull-comments --labels --discussions
    ```

- Inspect changes, `git add repositories/*`, `git commit`, `git push origin main`.
