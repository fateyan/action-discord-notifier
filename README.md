# Discord Notifier

A GitHub Action to post message to discord using discord webhook

This is a JavaScript action, so it should work on all machines include Windows, Linux, and macOS.

## Quick Example

```yaml
on:
  push:
    branches:
      - '**'

name: Discord Notification

jobs:
  notify:
    name: Discord Notification
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - uses: fateyan/action-discord-notifier@v1
        with:
          message-title: New Commits Pushed
          webhook: https://discordapp.com/api/00000000000/secret
```


For more about workflow configuration, please see [GitHub Help](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions).  

About Discord webhook, please see [this article on Discord Help Centre](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks).

## Usage

|Argument|Required|Description|
|---|---|---|
|webhook|✔️|A full webhook url. MUST NOT append `/github` at the end.|
|message-title|️ |Custom embed message title. Optional.|
