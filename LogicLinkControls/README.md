# LogicLink eisy BACnet Bridge
# Copyright (c) 2026 Steven Bailey / LogicLink. All rights reserved.

## Purpose

Native BACnet proof and future PG3/eisy bridge for LogicLink controllers.

This project is separate from `bacnet3_project`.

`bacnet3_project` remains the Bailey Gateway / Swift backend project.

This repo is for:

- eisy / FreeBSD BACnet discovery tests
- LogicLink BACnet device discovery
- BACnet object reads
- BACnet point value reads
- future BACnet writes
- future PG3 node creation
- future UDI / eisy integration

## Current Proof

Confirmed on eisy:

- Python 3.11 venv
- bacpypes 0.19.0
- BACnet Who-Is / I-Am discovery
- ReadProperty objectName
- ReadProperty objectList
- ReadProperty presentValue
- JSON output from BACnet reads

## eisy Test Environment

eisy IP:

```text
192.168.1.173


#
# LogicLink BACnet Priority Policy
#
# Dynamic Bridge uses BACnet Priority 3 for UDI/LogicLink supervisory commands.
#
# Priority Behavior:
#
#   P1-P2   Higher priority than Dynamic Bridge.
#           Local operator is LOCKED OUT.
#
#   P3      Dynamic Bridge Local command.
#           Used by UDI/LogicLink supervisory commands.
#
#   P4-P16  Lower priority than Dynamic Bridge.
#           Dynamic Bridge may temporarily take ownership by
#           writing Priority 3.
#
# When the Dynamic Bridge Priority 3 command is released, BACnet
# automatically restores the highest remaining active
# priority (for example an external Priority 9 command).
#
# This behavior follows the BACnet priority array standard
# while providing predictable local operator control.
#
