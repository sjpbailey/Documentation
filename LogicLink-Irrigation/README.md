# LogicLink Irrigation Plugin

LogicLink Irrigation is a production-oriented irrigation controller plugin designed to integrate LogicLink hardware with automation platforms using a backend-driven architecture.

This plugin is part of the LogicLink controller ecosystem and provides a structured, reliable interface for irrigation control, status reporting, and future BACnet-based integration.

---

## Project Purpose

This project provides the plugin layer for irrigation control within the LogicLink platform.

The architecture is:

- Local controller hardware
- LogicLink backend authority
- Plugin / node server integration
- Optional BACnet exposure
- Frontend control through automation platforms

---

## Design Goals

- Local-first control (no cloud dependency)
- Reliable zone operation
- Clear and accurate status reporting
- Safe manual and automated operation
- Re-nameable nodes for clean UI layout
- Separation of plugin and controller logic

---

## Architecture Position

This plugin is not the controller.

It is the integration layer between automation systems and LogicLink-controlled irrigation hardware.

All hardware control and state authority reside in the LogicLink backend.

---

## Node Model

The plugin uses a **node-per-zone model**.

This allows:

- Clean naming of zones
- Clear program logic in automation systems
- Independent control and status per zone

### Controller Node

Represents overall controller state:

- Online / offline
- Backend communication
- Discovery / refresh

---

### Zone Nodes

Each irrigation zone is a separate node:

- ON / OFF command
- Current state (backend-driven)
- Re-nameable in Admin Console
- Fully usable in automation programs

---

## Configuration

The plugin is configured using **Custom Parameters (JSON)**.

Three parameters are required:

- `controllers`
- `inputs`
- `zones`

---

### Example Configuration

```json
{
  "controllers": [
    {
      "id": "c1",
      "name": "Controller 1",
      "base_url": "http://192.168.1.50:8099"
    }
  ],
  "zones": {
    "c1": [
      { "id": 1, "name": "01 Zone 1", "bo": 1 },
      { "id": 2, "name": "02 Zone 2", "bo": 2 }
    ]
  }
}
