![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)
[![Validate with hassfest](https://github.com/submarcos/hassio-ecoflow/actions/workflows/hassfest.yml/badge.svg)](https://github.com/submarcos/hassio-ecoflow/actions/workflows/hassfest.yml)
[![HACS Action](https://github.com/submarcos/hassio-ecoflow/actions/workflows/hacs.yml/badge.svg)](https://github.com/submarcos/hassio-ecoflow/actions/workflows/hacs.yml)
[![CodeQL](https://github.com/submarcos/hassio-ecoflow/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/submarcos/hassio-ecoflow/actions/workflows/codeql-analysis.yml)

# EcoFlow Portable Power Station Integration for Home Assistant

This integration uses a local API.
Therefore, if the devices are not on the same network, they cannot synchronize their status.

This integration uses a private API.
Future device updates may prevent integration.

Requires Home Assistant Core 2022.7.0 or later for operation.

## Installation
This integration is not included by default and must be installed by yourself to use it.

Two methods are available, and you can choose one or the other.
- Install as a custom repository via HACS
- Manually download and extract to the custom_components directory

Once installed, after restarting Home Assistant, you can start integration as usual from Add Integration.

## Supported products
- ~~RIVER Mini~~ (Coming soon)
- RIVER Max
- RIVER Pro
  - Extra Battery
- DELTA Mini
- DELTA Max
  - with Extra Battery
- DELTA Pro (Wi-Fi only)
  - with Extra Battery

## How to register for the Energy Dashboard
- MPPT input energy : Solar Panels -> Solar production energy
- total input energy : Home Battery Storage -> Energy going in to the battery
- total output energy : Home Battery Storage -> Energy coming out of the battery

## About Remain Entities
The Remain entity is disabled by default because it is highly variable and generates a large number of writes to the database.

If enabled, it is recommended that these entities be included in the exclude in the recorder settings.
