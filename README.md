# SolidWorks

> Automates SolidWorks 3D CAD — modelling, sketches, assemblies, drawings, and exports — through this assistant. Needs SolidWorks installed on this computer.

The bundle zip (**72.6 MB**) is stored in this repository at **`3e135651-aaf0-43d1-8cc5-3ef5eeee6e59.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `3e135651-aaf0-43d1-8cc5-3ef5eeee6e59` |
| Status in registry | active |
| Bundle size | 72.6 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `SOLIDWORKS_PATH` | `C:\Program Files\SOLIDWORKS Corp\SOLIDWORKS` |
| `SOLIDWORKS_EXECUTION_URL` | `http://localhost:5000` |
| `EXECUTION_EXE_PATH` | `__INSTALL_DIR__/execution/solidworks/SolidworksExecution.exe` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "server.py"
  ],
  "env": {
    "SOLIDWORKS_EXECUTION_URL": "http://localhost:5000",
    "EXECUTION_EXE_PATH": "__INSTALL_DIR__/execution/solidworks/SolidworksExecution.exe",
    "SOLIDWORKS_PATH": ""
  }
}
```


## Install / usage

1. Get the bundle:
   - download `3e135651-aaf0-43d1-8cc5-3ef5eeee6e59.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
