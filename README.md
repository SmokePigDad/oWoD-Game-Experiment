# AI Dungeon Experiment with Roo Code

This repository serves as the central hub for managing AI Dungeon campaigns, character information, and Roo Code modes tailored for an immersive D&D-style RPG experience. It is designed to work in conjunction with a separate set of [RPG MCP Servers](https://github.com/Mnehmos/rpg-mcp-servers) that handle game mechanics and state persistence.

## Overview

The primary goal of this project is to leverage Roo Code's multi-agent capabilities to:
- Create and manage dynamic AI-driven narratives.
- Facilitate character creation and development.
- Store campaign-specific information and world-building details.
- Utilize specialized Roo modes for different aspects of game management (e.g., Dungeon Master, Character Creator, World Builder).

## Key Components

- **`.roomodes/`**: This directory (or file, depending on your setup) contains the configurations for custom Roo Code modes used to interact with and manage the AI Dungeon. These modes orchestrate tasks and communicate with the RPG MCP Servers.
- **Game Templates & Guides**:
    - `character-sheet.md`: A template for character sheets.
    - `dnd5e-character-creation-guide.md`: A guide for D&D 5th Edition character creation.
    - `combat-engine-spec.json`: (If applicable) Specifications or notes related to the combat engine.
- **`campaigns/`**: This directory is intended to store all your campaign-specific data, including world details, NPC information, adventure logs, and player character notes.
    - **Important**: The `campaigns/` directory is included in the `.gitignore` file. This is to prevent accidental commits of potentially large or private campaign data to this main repository. You should manage your campaign data in a separate version control system or backup solution if desired.

## RPG MCP Servers

The game mechanics, dice rolling, and persistent state (like character stats, inventory, and world state) are handled by a dedicated set of MCP (Model Context Protocol) servers. These servers run independently and provide tools that Roo Code modes can utilize.

For information on setting up and configuring these servers, please refer to the [rpg-mcp-servers GitHub repository](https://github.com/Mnehmos/rpg-mcp-servers).

## Getting Started

1.  **Set up the RPG MCP Servers**: Clone and configure the [rpg-mcp-servers](https://github.com/Mnehmos/rpg-mcp-servers) as per the instructions in their README. Ensure they are running and accessible to Roo Code.
2.  **Configure Roo Code**:
    - Ensure your Roo Code `mcp_settings.json` is correctly pointing to the running MCP servers.
    - Load the custom Roo modes (e.g., Dungeon Master, Character Creator) defined in this repository into your Roo Code environment.
3.  **Start a Campaign**:
    - Use the Character Creator mode to create new characters.
    - Use the World Builder mode (if available) to define your campaign setting.
    - Begin your adventure using the Dungeon Master mode to narrate and manage the game, interacting with the MCP servers for game mechanics.
4.  **Manage Campaign Data**: Store your campaign-specific files within the `campaigns/` directory. Remember this directory is ignored by Git in this repository.

This setup allows for a powerful separation of concerns: Roo Code and its AI modes handle the narrative, creativity, and user interaction, while the MCP servers manage the underlying game rules and data.