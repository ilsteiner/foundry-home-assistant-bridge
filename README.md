# Foundry VTT to Home Assistant Bridge

A bidirectional integration between Foundry Virtual Tabletop and Home Assistant, allowing you to enhance your tabletop gaming experience with smart home automation.

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg)](https://github.com/custom-components/hacs)
[![ha_version](https://img.shields.io/badge/Home%20Assistant-2023.1.0+-blue.svg)](https://www.home-assistant.io/)
[![foundry_version](https://img.shields.io/badge/Foundry%20VTT-11.0+-green.svg)](https://foundryvtt.com/)

## Project Overview

This project consists of two main components:

1. **Foundry VTT Module** (in `home-assistant-connect/`): A module for Foundry VTT that sends game data to Home Assistant
2. **Home Assistant Integration** (in `foundryvtt-connect/`): A custom component for Home Assistant that receives and processes data from Foundry VTT

## Features

- Send character stats (HP, AC, conditions, etc.) to Home Assistant
- Track combat events (start, end, turns, rounds)
- Create automations in Home Assistant based on game events
- Use smart home devices to enhance your gaming sessions with:
  - Dynamic lighting based on game events
  - Sound effects triggered by combat or character actions
  - Notifications for important game moments
  - Visual indicators for player turns and status effects

## Installation

### 1. Home Assistant Integration

#### One-Click Installation
[![Open your Home Assistant instance and show the add-on repository.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=ilsteiner&repository=foundryvtt-connect&category=integration)

After adding the repository to HACS:
1. Go to Settings > Devices & Services > Add Integration
2. Search for "Foundry VTT" and complete the setup
3. Note the webhook ID provided during setup

#### Manual Installation

1. Copy the `foundryvtt-connect/custom_components/foundry_vtt` directory to your Home Assistant `config/custom_components` directory
2. Restart Home Assistant
3. Go to Settings > Devices & Services > Add Integration
4. Search for "Foundry VTT" and complete the setup
5. Note the webhook ID provided during setup

### 2. Foundry VTT Module

1. Install via the Foundry VTT module browser or manually by copying the files
2. Enable the module in your world
3. Configure the module with your Home Assistant URL, access token, and webhook ID
4. Enable the integration

## Configuration

See the README files in each component directory for detailed configuration instructions:

- [Foundry VTT Module Configuration](./home-assistant-connect/README.md)
- [Home Assistant Integration Configuration](./foundryvtt-connect/README.md)

## Usage Examples

- Create immersive combat experiences with dynamic lighting
- Display character health and status on Home Assistant dashboards
- Set up alerts for critical character conditions
- Trigger sound effects based on game events
- Log game sessions and events for later reference

## Development

### Project Structure

- `home-assistant-connect/`: Foundry VTT module (TypeScript)
- `foundryvtt-connect/`: Home Assistant custom component (Python)

### Building the Project

```bash
# Build Foundry VTT module
cd home-assistant-connect
npm install
npm run build

# Home Assistant integration doesn't require building
```

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.