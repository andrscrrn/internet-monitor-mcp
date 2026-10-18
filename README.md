# Internet Monitor MCP server

Ask your AI how your internet has been. This MCP server connects Claude Desktop (or any MCP client) to [Internet Monitor: Uptime](https://internetmonitor.app), a menu bar app for macOS that checks your connection every second and keeps the evidence.

Once connected, you can ask things like:

- "How has my internet been today?"
- "List every outage this week with exact times"
- "What was my average latency yesterday, per network?"

## Tools

Five read-only tools, with periods up to 30 days and filterable per network:

| Tool | What it returns |
| --- | --- |
| `get_status` | Current connection state |
| `get_uptime` | Uptime summaries for a period |
| `list_outages` | Every outage with exact start, end, and duration |
| `get_latency_stats` | Latency statistics per probe target |
| `list_networks` | The networks your Mac has used |

## Install

1. Get [Internet Monitor: Uptime on the Mac App Store](https://apps.apple.com/app/apple-store/id6818842901?pt=127166683&ct=mcp&mt=8) (US$4.99, one-time). The app records the data the server reads; without it the server has nothing to report.
2. Download the one-click bundle from the [latest release](https://github.com/andrscrrn/internet-monitor-mcp/releases/latest) or from [internetmonitor.app/ai](https://internetmonitor.app/ai.html), then double-click it to install in Claude Desktop. The app's Settings also offer an Install Claude Extension shortcut.

Requires macOS 14 or later.

## Privacy

The server is a local stdio process that reads the app's locally stored monitoring files, nothing else. It is sandboxed, works even when the app is closed, opens no network ports, and sends nothing anywhere. The app itself ships with App Privacy: Data Not Collected.

## About this repository

Internet Monitor is a commercial app, so this repository hosts the release bundles and this page, not the source code. Questions and bug reports: [internetmonitor.app/support](https://internetmonitor.app/support.html).
