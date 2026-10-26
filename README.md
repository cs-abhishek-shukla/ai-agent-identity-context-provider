# Release Information

- **Version**: 1.0.1

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Context and Enrichment, Triage

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

- [Release Notes](./release_notes.md)

# Identity Context Provider

Enriches user identities with role, privilege level, group memberships, behavior patterns, and recent authentication activity to assess user risk and investigate user-related incidents.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

The Identity Context Provider agent ships with a configuration that has access to all shipped MCP servers. For custom configuration, refer to the *Configuration* section of the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor) solution pack documentation.

> [!Note]
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.

### Prerequisites

The following prerequisites must be met before using this agent:

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
> The FortiAI solution pack and the Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.1` and later.

## Input Parameters

The input must be provided as a JSON object.

| Parameter  | Description                                                       |
|------------|-------------------------------------------------------------------|
| `question` | The question to be answered.                                      |
| `user`     | A username or a user ID for which the question is to be answered. |

## Response

The output is returned as a JSON object.

| Parameter    | Description                                                                       |
|--------------|-----------------------------------------------------------------------------------|
| `answer`     | Answer to the query derived from available data.                                  |
| `confidence` | Confidence percentage indicating reliability of the answer (For example: *85%*). |
| `evidence`   | Supporting information and details from retrieved data sources.                  |