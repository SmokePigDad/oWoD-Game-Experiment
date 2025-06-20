# AI World of Darkness Experiment with Roo Code

This repository is the central hub for running interactive, AI-driven World of Darkness chronicles using Roo Code. It contains the AI instructions, character sheet templates, and campaign files needed to bring the gothic-punk world to life.

This project works in conjunction with the [Unified WoD MCP Servers](https://github.com/SmokePigDad/rpg-mcp-servers), which handle all game mechanics and data persistence.

## Overview

The goal of this project is to create a truly interactive and visually rich storytelling experience. Instead of just commanding an AI, you will be guided through the story with meaningful choices. The AI acts as your personal Storyteller, managing the rules and narrative, while you make all the important decisions for your character.

### **Newest Features!**
- **Graphical HTML Character Sheets:** Generate a full, beautifully styled character sheet that looks like it's straight from a sourcebook.
- **Visual Health Tracker:** Instantly see your character's damage levels and wound penalties in a clear, thematic format.
- **Rules-Enforced XP Spending:** Spend experience points through a guided, interactive menu where the costs are calculated and enforced by the server, ensuring game balance.

## The Interactive Gameplay Loop

This project is built around a core "Describe -> Ask -> Resolve" loop:
1.  **Describe:** The Storyteller AI sets the scene.
2.  **Ask:** The AI pauses and presents you with a set of clear, meaningful choices on how your character can act.
3.  **Resolve:** Once you choose, the AI uses powerful backend tools to resolve the action's mechanics and then narrates the rich outcome.

**Example:**
> **AI Storyteller:** The thug takes a swing at you! *(The AI calls `resolve_attack`, which handles all the dice rolls internally)*. The attack connects! He suffers 2 levels of bashing damage.
>
> *(The AI then calls `display_health`)*
>
> **AI Storyteller:** Here is his current status:
> Health Status:
> `[X][X][/][/][ ][ ][ ] Wounded (-2)`
>
> He's looking hurt. What do you do?
> **[A]** Press the attack.
> **[B]** Try to talk him down.
> **[C]** Flee the scene.

## Key Components

- **`.roomodes`**: Contains the configuration for the `💀 WoD Storyteller (Interactive)` AI mode. This file is the "brain" of the AI.
- **`character-sheet-wod-template.md`**: A markdown template used as a base for character notes.
- **`wod-quickstart-guide.md`**: A guide explaining the mechanics and how to interact with the Storyteller AI.
- **`campaigns/`**: Where your campaign-specific data will be stored by the AI. (Note: This directory is in `.gitignore`).

## Getting Started

1.  **Set up the MCP Servers**: Clone and configure the [Unified WoD MCP Servers](https://github.com/SmokePigDad/rpg-mcp-servers) as per the instructions in their README. Ensure both servers are running.
2.  **Configure Roo Code**:
    - Ensure your Roo Code `mcp_settings.json` is correctly pointing to the running MCP servers.
    - Open this folder (`oWoD-Game-Experiment`) as your workspace root in VS Code. Roo Code will automatically detect and load the Storyteller mode.
3.  **Start a Chronicle**:
    - Activate the `💀 WoD Storyteller (Interactive)` mode in Roo Code.
    - Ask the AI to create a character. It will guide you through the process interactively.
    - Ask it to "generate a fancy character sheet" to see the new HTML feature!
