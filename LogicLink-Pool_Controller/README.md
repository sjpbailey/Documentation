# LogicLink Pool Controller

LogicLink Pool Controller integration and PG3/eisy showcase build.

This project demonstrates:

- Pool Controller web interface
- Pump Portal integration
- Scheduler integration
- PG3/eisy integration
- API-first architecture
- Multi-service local automation architecture
- BACnet integration direction for future LogicLink systems

---

## System Architecture

| Service | Port | Description |
|---|---|---|
| Front Page | 8098 | LogicLink Front Launcher |
| Pump Portal | 8080 | Pump control system |
| Pool Controller | 8081 | Pool automation controller |
| Scheduler | 9090 | Pump scheduler |
| LL8 Config/API | 8099 | Hardware I/O and configuration |

---

## Screenshots

## LogicLink Front Page (8098)

![LogicLink Front](images/front-8098.png)

---

## Pump Portal (8080)

![Pump Portal](images/pump-8080.png)

---

## Pool Controller (8081)

![Pool Controller](images/controller-8081.png)

---

## Scheduler (9090)

![Scheduler](images/schedule-9090.png)

---

## Current Features

- Live equipment status
- Pool temperatures
- Air temperatures
- Source temperatures
- Filter PSI monitoring
- Heater enable status
- Heater firing status
- Pump proof status
- Pool light control
- Schedule armed status
- Local API integration
- PG3/eisy node server integration

---

## PG3 / eisy Integration

The LogicLink Pool PG3 integration currently supports:

- Live status updates
- Equipment control commands
- Local API communication
- Admin Console status display
- PG3 custom parameter configuration

---

## Future Direction

Future LogicLink development includes:

- True BACnet discovery
- BACnet application grouping
- Unified frontend navigation
- LogicLink controller builder integration
- Multi-controller system architecture
- Graphics/programming frontend
- Additional automation systems

---

## Development Status

This repository contains an internal LogicLink development build intended for evaluation, testing, and integration development with authorized LogicLink hardware and controller systems.

LogicLink hardware, firmware, and software are currently under active development and are not yet released as general-purpose consumer products.

This software is tightly coupled to LogicLink controller architecture and is not intended to function as a standalone public solution without compatible LogicLink hardware, services, and supporting infrastructure.

The repository is provided primarily for development documentation, architecture review, API integration reference, and UDI/eisy integration evaluation.

## License

See [LICENSE](LICENSE)
