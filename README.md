# RTI AI CLI — Releases and Feedback

Use `rtiai` to inspect and troubleshoot DDS systems with Run-Time Expert (RTE), or to ask Connext AI questions from your terminal with RTI AI Chat. This repository is where RTI publishes CLI downloads and tracks bug reports, feature requests, and questions.

## Download the CLI

The first CLI release is pending. Once it is available, download the archive for your operating system and processor, along with `checksums.txt`, from [Releases](https://github.com/realtimeinnovations/rtiai-cli-feedback/releases).

Verify the archive’s SHA-256 checksum against its entry in `checksums.txt`, extract `rtiai` (`rtiai.exe` on Windows), and place it in a directory on your `PATH`. Run `rtiai --version` to check the installation.

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
