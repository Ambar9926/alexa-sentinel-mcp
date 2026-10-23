# Alexa+ Sentinel: Multi-Device MCP Orchestrator

Built for the **Build, Ship, Shape: Amazon Developer Hackathon** (**Primary Track: Alexa+**).

## Overview
**Alexa+ Sentinel** combines a self-hosted **Model Context Protocol (MCP Spec 2025-11-25, Streamable HTTP)** server (`mcp_server.py`) with an interactive **Alexa+ Web Simulation Console** (`index.html`). It demonstrates how Alexa+ acts as an autonomous agent connecting the living room (Fire TV), the front door (Ring), and personal wearable context (Bee).

## Architecture & Key Features
- **MCP Server (`mcp_server.py` & `mcp_config.json`):** Built using `FastMCP` with `streamable-http` transport exposing four multi-device tools (`ring_door_control`, `firetv_launch_mode`, `bee_context_sync`, and `aws_security_audit`).
- **Interactive Web Simulator (`index.html`):** Visualizes real-time JSON-RPC 2.0 MCP tool calls, device state transitions, and synthesized English voice responses from Alexa+.

## How to Run
### 1. Run the Interactive Web Simulation (Zero-Setup)
Open `index.html` directly in any modern browser (Chrome, Edge, Firefox) and click **"Run Automated English Walkthrough"** or click individual scenario triggers.

### 2. Run the Self-Hosted MCP Server (Optional Backend)
```bash
pip install mcp
python mcp_server.py