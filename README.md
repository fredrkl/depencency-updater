# Depencency Updater

This repository contains a setup for [Renovate](https://docs.renovatebot.com/)
to automate the process of updating dependencies. It runs as a custom GitHub
Application that only has access to the repositories it is monitoring. The
GitHub app is installed on my profile.

I followed the guide on [Running as a GitHub
App](https://docs.renovatebot.com/modules/platform/github/#running-as-a-github-app)
in order to have full control over the repositories Renovate is monitoring.

## Monitoring new repository

In order to monitor a new repository, you need to give the GitHub App access by
extending the list on: <https://github.com/settings/installations/77373733>.
Renovate is running using the autodiscovery feature, so it will automatically
start monitoring all repositories it has access to.
