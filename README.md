# Depencency Updater

This repository contains a setup for [Renovate](https://docs.renovatebot.com/)
to automate the process of updating dependencies. It runs as a custom GitHub
Application that only has access to the repositories it is monitoring. The
GitHub app is installed on my profile.

## Monitoring new repository

In order to monitor a new repository, you need to give the GitHub App access by
extending the list on: <https://github.com/settings/installations/77373733>.
Additionally, you need to add the repository to the `renovate.json` file in
this repository.
