# Depencency Updater

This repository contains a setup for [Renovate](https://docs.renovatebot.com/)
to automate the process of updating dependencies. It runs as a custom GitHub
Application that only has access to the repositories it is monitoring. The
GitHub app is installed on my profile.

I followed the guide on [Running as a GitHub
App](https://docs.renovatebot.com/modules/platform/github/#running-as-a-github-app)
in order to have full control over the repositories Renovate is monitoring.

It is possible to install the [Renovate GitHub
App](https://github.com/marketplace/renovate) on your own profile or
organization instead. However, I wanted to showcase and have full control over
the Renovate setup, so I decided to run it as a custom GitHub App.

This repo has the Renovate _APP ID_ and the _private key_ as _repository
secrets_ to authenticate the application. Please see the
[renovate.yml](.workflows/renovate.yml) and the
[./renovate.json](./renovate.json) files for the configuration. [Self hosted
configuration
options](https://docs.renovatebot.com/self-hosted-configuration/#self-hosted-configuration-options)
are configured using environment variables in the workflow. Other settings are
configured in the `renovate.json` file.

## Monitoring new repository

In order to monitor a new repository, you need to give the GitHub App access by
extending the list on: <https://github.com/settings/installations/77373733>.
Renovate is running using the autodiscovery feature, so it will automatically
start monitoring all repositories it has access to.
