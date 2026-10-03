# Azure Resiliency Agent

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Agent Plugins](https://img.shields.io/badge/format-Agent%20Plugins%201.0-5b9bff.svg)](https://agent-plugins.org/)
[![Microsoft Azure](https://img.shields.io/badge/Microsoft-Azure-0078d4.svg)](https://azure.microsoft.com/)

The Azure Resiliency Agent plugin brings Azure's Start Resilient experience into GitHub Copilot.
It helps customers assess application architectures, generate new zone-resilient
infrastructure-as-code, and review existing Bicep, ARM JSON, and Terraform.

The plugin uses the Azure MCP Server to invoke the authoritative Azure Resiliency Agent while
preserving native GitHub Copilot repository, editing, validation, and source-control workflows.

## Capabilities

| Capability | Outcome |
| --- | --- |
| Architecture assessment | Assess a described Azure application architecture for availability-zone resiliency |
| IaC generation | Generate new resilient Bicep, ARM JSON, or Terraform |
| Bicep review | Review and correct existing Bicep and its local modules |
| ARM review | Review and correct existing ARM JSON and parameter files |
| Terraform review | Review and correct existing Terraform modules and variables |
| Local file handoff | Share selected local files with explicit user approval and bounded local processing |

## How it works

1. Select **AzureResiliencyAgent** in GitHub Copilot.
2. Describe the architecture or infrastructure-as-code task.
3. The agent invokes the matching Azure Resiliency tool.
4. If local files are required, the plugin asks for approval before each file is read and prepared.
5. The hosted Azure Resiliency Agent returns authoritative findings, reports, and corrected content.
6. GitHub Copilot can apply approved corrections through its native diff and Keep/Undo experience.

## Prerequisites

- A supported GitHub Copilot host with Agent Plugins and local stdio MCP support.
- Node.js and `npx` available on `PATH`.
- An Azure sign-in through a supported delegated developer credential such as Azure CLI,
  Azure PowerShell, Visual Studio Code, or Visual Studio.

## Development

Load the repository as a local Agent Plugin while developing:

```powershell
copilot --plugin-dir <path-to-this-repository> --agent azure-resiliency-agent:AzureResiliencyAgent
```

The committed `mcp.json` uses the published `@azure/mcp` package. Before the Azure MCP release that
contains the Resiliency Agent tools is available, use a local, uncommitted test override that points
to the corresponding Azure MCP build.

## Security

Do not report security vulnerabilities through public GitHub issues. See [SECURITY.md](SECURITY.md).

## Contributing

The repository is currently maintained by the Azure Resiliency Agent team. Contribution guidance
will be expanded as the plugin approaches public marketplace availability.

## License

MIT. See [LICENSE](LICENSE).
