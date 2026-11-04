# Changelog

All notable changes to the Azure Resiliency Agent plugin are documented in this file.

## [0.1.1] - 2026-11-04

### Changed

- Answer plugin capability and scope questions without invoking Azure Resiliency tools.
- Keep advertised capabilities limited to the workflows available through the plugin.
- Update Azure Copilot terminology and customer prerequisites.
- Add Node.js, npm, and npx verification guidance.
- Correct the GitHub Copilot CLI agent identifier.

## [0.1.0] - 2026-10-03

### Added

- Initial Agent Plugins 1.0 package.
- `AzureResiliencyAgent` custom agent.
- Azure MCP Server registration scoped to the `resiliencyagent` namespace.
- Architecture assessment, IaC generation, and Bicep, ARM, and Terraform review workflows.
- Explicitly approved local file handoff workflow.
