# RTI AI CLI — Releases and Feedback

Use `rtiai` to inspect and troubleshoot DDS systems with Run-Time Expert (RTE), or to ask Connext AI questions from your terminal with RTI AI Chat. This repository is where RTI publishes CLI downloads and tracks bug reports, feature requests, and questions.

## Download the CLI

The standalone CLI runs on macOS and Linux (Intel/AMD 64-bit and ARM64) and Windows x64.

### macOS and Linux

Run the shell installer in a terminal.

```sh
curl -fsSL https://github.com/realtimeinnovations/rtiai-cli-feedback/releases/latest/download/install.sh | sh
```

The installer verifies the archive’s SHA-256 checksum and installs to `/usr/local/bin` by default. For a per-user installation, pipe the download to `env INSTALL_DIR="$HOME/.local/bin" sh` and add that directory to your `PATH`.

### Windows

Run the installer in PowerShell, then open a new terminal so it picks up your updated `PATH`.

```powershell
irm https://github.com/realtimeinnovations/rtiai-cli-feedback/releases/latest/download/install.ps1 | iex
```

### Homebrew

If RTI’s tap lists `rtiai`, run the following commands on macOS or Linux. If the formula is unavailable, use the shell installer above. [Browse RTI’s Homebrew formulas](https://github.com/realtimeinnovations/homebrew-tap/tree/main/Formula)

```sh
brew tap realtimeinnovations/tap
brew install rtiai
```

### Manual installation

Download the archive for your operating system and processor, along with `checksums.txt`, from [Releases](https://github.com/realtimeinnovations/rtiai-cli-feedback/releases). Verify the archive’s SHA-256 checksum against its entry, extract `rtiai` (`rtiai.exe` on Windows), and place it in a directory on your `PATH`.

Run `rtiai --version` to verify the installation. To check for updates, run `rtiai update --check`. Upgrade a standalone macOS or Linux installation with `rtiai update`. For Homebrew, run `brew upgrade rtiai`. On Windows, rerun the PowerShell installer.

## Get started

Run `rtiai setup` and choose RTE, Chat, or both.

- **Run-Time Expert** lets AI tools inspect your DDS system. Set `CONNEXT_CLOUD_API_KEY` to your RTI Cloud service-account key in the shell where you run `rtiai rte start`. Startup prints the MCP endpoint for connecting your tools. Use `rtiai rte status` to check connections and `rtiai rte stop` to stop RTE.
- **RTI AI Chat** connects to the experts you select during setup. Choose your model provider and set its API-key environment variable if required. Run `rtiai chat` to start a conversation. You can use Chat with Connext AI on its own or connect it to RTE.

Run `rtiai --help` to explore commands or `rtiai doctor` to check your setup.

## Submit feedback

Search the [existing issues](https://github.com/realtimeinnovations/rtiai-cli-feedback/issues) for your topic. Add details to a matching issue or [open a new issue](https://github.com/realtimeinnovations/rtiai-cli-feedback/issues/new).

- **Bug report** — Include the output of `rtiai --version`, your operating system and architecture, the command and steps that reproduce the problem, and what you expected and observed. If you share logs, remove API keys, tokens, and private DDS data first.
- **Feature request** — Describe what you want to accomplish and where the CLI falls short today.
- **Question or other feedback** — Tell us which command or part of your workflow you have a question or suggestion about.

For broader Connext questions and reference material, visit the [RTI Community Forum](https://community.rti.com/) or [RTI Documentation](https://community.rti.com/documentation).
