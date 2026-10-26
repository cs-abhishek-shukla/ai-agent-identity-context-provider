# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Context and Enrichment, Triage

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

# Identity Context Provider

Enriches user identities with role, privilege level, group memberships, behavior patterns, and recent authentication activity to assess user risk and investigate user-related incidents.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

**Required MCP Servers**: SOC Framework

> [!Note]
>
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.
> 

### Prerequisites

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
>
> FortiAI solution pack and Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.0`.
> 


## Input Parameters

The input must be provided as a JSON object.

| Parameter  | Description                                                       |
|------------|-------------------------------------------------------------------|
| `question` | The question to be answered.                                      |
| `user`     | A username or a user ID for which the question is to be answered. |


## Response

The output is returned as a JSON object.

| Parameter    | Description                                                       |
|--------------|-------------------------------------------------------------------|
| `status`     | Indicates whether the request completed successfully or failed.   |
| `confidence` | List of records returned from the FortiSOAR based on the request. |
| `evidence`   | Supporting information and details from retrieved data sources.   |

