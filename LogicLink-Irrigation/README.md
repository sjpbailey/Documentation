# LogicLink Irrigation Plugin

LogicLink Irrigation is a production-oriented irrigation controller plugin designed to connect local irrigation hardware into a clean control system interface.

This plugin is part of the LogicLink controller ecosystem and is intended to support reliable local automation, clear status reporting, and future BACnet-based controller integration.

## Project Purpose

This project provides the plugin layer for irrigation control.

The long-term architecture is:

- Local controller hardware
- LogicLink backend authority
- Plugin / node server integration
- Optional BACnet discovery and mapping
- Frontend control through supported automation platforms

## Design Goals

- Local-first control
- Reliable irrigation zone operation
- Clear controller status
- Safe manual and automatic operation
- Production-ready documentation
- Separation between plugin code and proprietary controller code

## Architecture Position

This plugin is not the entire LogicLink controller platform.

It is the integration layer that allows an automation system to communicate with LogicLink-controlled irrigation equipment.

The controller firmware, BACnet controller logic, hardware abstraction, and product-specific controller code remain part of the LogicLink controller platform.

## Planned Capabilities

- Discover supported LogicLink irrigation controllers
- Read zone status
- Read controller mode
- Start and stop zones
- Support automatic scheduling logic where applicable
- Expose usable status values to the automation frontend
- Support future BACnet-backed discovery and mapping

## BACnet Direction

LogicLink controllers are being designed around a BACnet-capable architecture.

The intended model is:

1. Controller owns the hardware state
2. Backend discovers and caches controller points
3. Plugin reads status from the backend
4. Commands are routed through controlled API endpoints
5. Frontend systems consume mapped points safely

This keeps the control authority in one place while allowing external systems to display and operate the controller.

## Development Status

This project is under active development.

Current focus:

- Finalize irrigation controller behavior
- Lock backend API patterns
- Document controller/plugin responsibilities
- Prepare production plugin structure

## Ownership

Copyright (c) 2026 Steven Bailey / LogicLink.  
All rights reserved.

This project and its related controller software are owned by LogicLink.

## License

See `LICENSE.md`

Add it as text first. Screen captures help later, but the repo needs copyable examples.

Put this near the bottom:

## Project Status

Initial documentation and licensing established.

Next steps:

- Define backend API contract
- Implement irrigation controller plugin structure
- Integrate with LogicLink backend

## Hardware Availability

This plugin is designed to operate with LogicLink irrigation controllers.

LogicLink controllers are deployed using a pre-configured runtime environment that includes controller logic, BACnet integration, and supporting system services.

### Deployment Model

Supported deployment approaches include:

- Pre-provisioned LogicLink controller hardware
- Customer-supplied hardware with LogicLink runtime installation

The LogicLink runtime is distributed as part of a controlled and licensed deployment.

While standard hardware components may be user-supplied, full functionality requires a LogicLink runtime environment.

This plugin may be installed and reviewed, but full operation requires a supported LogicLink controller.

For evaluation, integration discussions, or early access, please contact LogicLink.

## Example Node / Zone Mapping

The plugin separates the controller node from the zone nodes.

### Controller Node

The controller node represents the irrigation controller itself.

Typical controller values include:

- Online / offline status
- Current mode
- Discovery command
- Global controller health
- Backend communication status
Example concept:

```json
{
  "node": "controller",
  "name": "LogicLink Irrigation Controller",
  "status": true,
  "mode": "AUTO",
  "backend": "online"
}
```

## Zone Node

Each irrigation zone is represented as its own node.

A zone node may expose:

 Zone on/off status
 Zone name
 Manual start command
 Manual stop command
 Runtime remaining
 Schedule status
 Fault or disabled state

Example concept:

```json
{
  "node": "zone_1",
  "name": "Front Lawn",
  "zone_number": 1,
  "status": "OFF",
  "enabled": true,
  "runtime_seconds": 900,
  "remaining_seconds": 0,
  "schedule_active": true
}
```

Example Backend JSON

The backend is the authority for controller state.

The plugin should read from backend JSON instead of guessing hardware state.

Example controller response:

``` json
{
  "controller": {
    "online": true,
    "mode": "AUTO",
    "active_zone": null,
    "last_update": "2026-04-29T00:00:00Z"
  },
  "zones": [
    {
      "id": 1,
      "name": "Front Lawn",
      "enabled": true,
      "state": "OFF",
      "remaining_seconds": 0
    },
    {
      "id": 2,
      "name": "Back Yard",
      "enabled": true,
      "state": "OFF",
      "remaining_seconds": 0
    }
  ]
}
```

Command Model

Commands should be routed through backend endpoints.

The plugin should not directly own hardware control.

Example commands:

```json
{
  "command": "start_zone",
  "zone": 1,
  "runtime_seconds": 900
}
{
  "command": "stop_zone",
  "zone": 1
}
```

## Contact

For questions, integration discussions, or early access to LogicLink hardware:

Please use the Universal Devices (UDI) community forum or messaging system to reach out.

Commercial inquiries and partnership opportunities are welcome.
