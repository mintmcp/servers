# MintMCP

MintMCP is a product from the Lutra team. We create tools to help connect AI to data and apps. We have provided MCP servers below that make it easy to connect your favorite AI agent (Claude, Cursor, Windsurf, ChatGPT) to email and calendar apps.

When you connect to one of our servers, you will be asked to login using either your Google or Microsoft accounts, no additional accounts on MintMCP are required to use them.

## MCP Servers Available

### Google Calendar

- **Server URL:** `https://gcal.mintmcp.com/mcp`
- **Tools:**
  - create_event
  - delete_event
  - get_calendar_events
  - get_next_availability
  - list_calendars
  - update_event

**Configuration:**
```json
{
  "mcpServers": {
    "google-calendar": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://gcal.mintmcp.com/mcp"
      ]
    }
  }
}
```

### Gmail

- **Server URL:** `https://gmail.mintmcp.com/mcp`
- **Tools:**
  - draft_email
  - draft_reply
  - get_email
  - search_email
  - send_draft

**Configuration:**
```json
{
  "mcpServers": {
    "gmail": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://gmail.mintmcp.com/mcp"
      ]
    }
  }
}
```

### Outlook Calendar

Manage event listing, reading, and updates.

- **Server URL:** `https://outlook-calendar.mintmcp.com/mcp`
- **Tools:**
  - create_event
  - delete_event
  - get_calendar_events
  - get_next_availability
  - list_calendars
  - update_event

**Configuration:**
```json
{
  "mcpServers": {
    "outlook-calendar": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://outlook-calendar.mintmcp.com/mcp"
      ]
    }
  }
}
```

### Outlook

Search, read, and draft emails and replies.

- **Server URL:** `https://outlook-email.mintmcp.com/mcp`
- **Tools:**
  - draft_email
  - draft_reply
  - get_email
  - search_email
  - send_email

**Configuration:**
```json
{
  "mcpServers": {
    "outlook-email": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "https://outlook-email.mintmcp.com/mcp"
      ]
    }
  }
}
```

## MCP Gateway

For teams using MCP servers, managing authentication, monitoring, and configuration across multiple servers becomes operationally complex. It can be hard to understand which MCP servers your team is using, how they are using it, and whether the servers are secure. MCP gateways help by providing a control plane for your organization which give you the telemetry and governance you need. Learn more at [https://mintmcp.com](https://mintmcp.com)

Individual MCP servers don't include authentication, authorization, or audit logging. MintMCP's gateway consolidates multiple MCP servers behind a single authenticated endpoint. Instead of configuring each MCP server separately, clients connect to one gateway that routes requests to the appropriate underlying servers based on tool calls.
