# sosig

Slack-tO-diScord brIdGe

## Installation

This is not well-documented at the moment, sorry – essentially you have
to create a "classic app" in the Slack workspace you want to bridge and
create an application on Discord (at a minimum, it needs to be able to
send messages and manage webhooks), then put the tokens for each service
in the config file.

## Configuration

Currently you have to pass the path to the config file to sosig when you
run it (as in `sosig sosig.toml`). The config file should look something
like this:

```toml
[DiscordEndpoint]
token = "..."

[SlackEndpoint]
token = "xoxb-..."

[[room]]
endpoints = [
    { name = "DiscordEndpoint", location = "general" },
    { name = "SlackEndpoint", location = "general" },
]
```

## Contributing

Contributions are welcome!

Everyone interacting with this project is expected to abide by the terms
of the Contributor Covenant Code of Conduct. Violations should be
reported to coc-enforcement-sosig@sorrel.sh.

## Copyright

Copyright © 2020 Ash Holland. Licensed under the EUPL (1.2 or later).
