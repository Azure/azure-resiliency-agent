# Azure Resiliency Agent

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Agent Plugins](https://img.shields.io/badge/format-Agent%20Plugins%201.0-5b9bff.svg)](https://agent-plugins.org/)
[![Microsoft Azure](https://img.shields.io/badge/Microsoft-Azure-0078d4.svg)](https://azure.microsoft.com/)

Use Azure Resiliency Agent to validate deployment templates and identify resiliency gaps before
deployment. The plugin helps you assess an Azure application architecture, generate new resilient
infrastructure-as-code, and review existing Bicep, ARM JSON, and Terraform.

[Learn more about Azure Resiliency Agent in GitHub Copilot.](https://aka.ms/AzureResiliencyAgentInGithubCopilot)

## Capabilities and example prompts

| Capability | Outcome | Example prompt |
| --- | --- | --- |
| Architecture assessment | Assess a described Azure application architecture for availability-zone resiliency | `Assess this application architecture for availability-zone resiliency.` |
| IaC generation | Generate new resilient Bicep, ARM JSON, or Terraform | `Generate zone-resilient Bicep for this application architecture in East US 2.` |
| Bicep review | Review and correct existing Bicep and its local modules | `Review main.bicep, its local modules, and parameter file for availability-zone resiliency.` |
| ARM review | Review and correct existing ARM JSON and parameter files | `Review this ARM template and parameter file for resiliency gaps.` |
| Terraform review | Review and correct existing Terraform modules and variables | `Review this Terraform root module and its local child modules for zone resiliency.` |
| File-based assessment | Use selected architecture and infrastructure files after explicit approval | `Use architecture.md and the referenced deployment files to assess this application.` |

## Install from the Awesome Copilot marketplace

### Visual Studio Code

1. Open the **Extensions** view.
2. Search for:

   ```text
   @agentPlugins azure-resiliency-agent
   ```

3. Select **Azure Resiliency Agent** and choose **Install**.
4. Open GitHub Copilot Chat and select **AzureResiliencyAgent** from the agent picker.

If Agent Plugins are not visible, confirm that the VS Code setting `chat.plugins.enabled` is
enabled.

### GitHub Copilot CLI

Browse the Awesome Copilot marketplace:

```text
copilot plugin marketplace browse awesome-copilot
```

Install the plugin:

```text
copilot plugin install azure-resiliency-agent@awesome-copilot
```

Start GitHub Copilot CLI with the agent selected:

```text
copilot --agent azure-resiliency-agent:AzureResiliencyAgent
```

You can also select **AzureResiliencyAgent** from the interactive `/agent` menu.

## Try it

After selecting **AzureResiliencyAgent**, describe the application or deployment templates you want
to assess. For example:

- `Assess this App Service, PostgreSQL, and Redis architecture for availability-zone resiliency.`
- `Generate resilient Terraform for a web application with App Service and PostgreSQL.`
- `Review the Bicep files in infra/ and correct the zone-resiliency gaps.`
- `Review this ARM template without changing its existing resources or parameter names.`
- `Use this architecture diagram to identify resiliency gaps before deployment.`

When local files are needed, the plugin asks for approval before each selected file is shared for
analysis.

## Security

Do not report security vulnerabilities through public GitHub issues. See [SECURITY.md](SECURITY.md).

## Contributing

This plugin is maintained by the Azure Resiliency Agent team.

## License

MIT. See [LICENSE](LICENSE).
