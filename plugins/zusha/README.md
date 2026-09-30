# Zusha for Claude

Zusha (זושא) is the conversational learning companion for
[סְבֹרֶא](https://daily.knafaim.app/). It connects Claude to Sabra's hosted MCP
server for daily Jewish learning, source context, zmanim, communities, and
minyanim. A connected learner can also access personal features that are
currently enabled for their account, such as progress, reminders, and quizzes.

## Connection and privacy

The plugin points to `https://mcp.daily.knafaim.app/mcp` using MCP Streamable
HTTP. Public read tools can work without signing in. Personal information and
all changes require your own Sabra account, OAuth consent, and the relevant
server-side permission. Installing the plugin does not grant manager or
administrator access. Actions that change data retain an explicit approval
step before execution.

The plugin contains no API keys, client secrets, or stored account tokens. The
server's privacy policy is at [daily.knafaim.app/privacy](https://daily.knafaim.app/privacy).

## Data handling

The plugin bundle has no local scripts or account-data store. Tool requests go
from Claude to Sabra's declared MCP server, and tool results return to Claude.
With an account connection, those results can include your study plan and
progress, reminders, and quiz history. Sabra retains account data while the
account is active and deletes it when you delete the account. Its MCP server
does not store conversation content or a location supplied in a conversation.
For rate limiting, it may keep an IP address in memory for up to one hour;
operational logs contain the tool name, status, response time, random request
identifier, and server version, without request content. Sabra's privacy
policy describes its other service providers and data rights. Claude handles
your conversations and tool results under
[Anthropic's privacy policy](https://www.anthropic.com/legal/privacy).

## Install

In Claude, add Zusha from the plugin directory and connect the Zusha connector
from the plugin's Connectors tab. Sign in to Sabra when Claude asks you to
connect your account. In Claude Code, you can also install from this GitHub
marketplace:

```text
/plugin marketplace add ShalomMaman/zusha-plugin
/plugin install zusha@sabra
```

If you only want the remote MCP connection in Claude Code, add
`https://mcp.daily.knafaim.app/mcp` as an HTTP server named `zusha`.

Support: [daily.knafaim.app](https://daily.knafaim.app/).
