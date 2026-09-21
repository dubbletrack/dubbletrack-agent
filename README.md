# Dubbletrack Agent

Sends what your automation system plays to Dubbletrack and feeds RDS encoders. Runs on the computer that can see your automation system's logs or database.

## Install

**Mac and Debian / Ubuntu** (installs the headless command-line agent when there is no display):

    curl -fsSL https://github.com/dubbletrack/dubbletrack-agent/releases/latest/download/install.sh | sh

**Windows** (PowerShell):

    irm https://github.com/dubbletrack/dubbletrack-agent/releases/latest/download/install.ps1 | iex

Or download an installer from the [latest release](https://github.com/dubbletrack/dubbletrack-agent/releases/latest): the `.dmg` for Mac, the `x64-setup.exe` (or `.msi` for managed installs) for Windows, and the `Dubbletrack.Agent_*.deb` for a Debian or Ubuntu desktop. `dubbletrack-agent_*.deb` is the headless agent for a server without a display.

The desktop app updates itself. The headless agent is updated by running the install script again.

## Headless setup

After installing on a server, walk through connecting to your station and adding a source or encoder, then start the service:

    dubbletrack-agent setup
    sudo systemctl enable --now dubbletrack-agent

`dubbletrack-agent --help` lists the other commands, including `status`, `list`, and `test` for sending text to an encoder.
