# AI World of Darkness Experiment with Roo Code

> **_Updated for the new World of Darkness project overhaul (June 2025)._**
This repository is the central hub for running interactive, AI-driven World of Darkness chronicles using Roo Code. It contains the AI instructions, character sheet templates, and campaign files needed to bring the gothic-punk world to life.

This project works in conjunction with the [Unified WoD MCP Servers](https://github.com/Mnehmos/rpg-mcp-servers), which handle all game mechanics and data persistence.

## Overview

The goal of this project is to create a truly interactive storytelling experience. Instead of just commanding an AI, you will be guided through the story with meaningful choices. The AI acts as your personal Storyteller, managing the rules and narrative, while you make all the important decisions for your character.

## The Interactive Gameplay Loop

This project is built around a core "Describe -> Ask -> Resolve" loop:
1.  **Describe:** The Storyteller AI sets the scene, describing the environment and situation.
2.  **Ask:** The AI pauses the narrative and presents you with a set of 3-5 clear, meaningful choices on how your character can act, using an interactive prompt.
3.  **Resolve:** Once you make a choice, the AI uses the backend MCP servers to resolve the action's mechanics (dice rolls, resource costs, etc.) and then narrates the outcome, seamlessly continuing the story.

**Example:**
> **AI Storyteller:** The bouncer blocks your path, his arms crossed. 'Private party,' he grunts. 'No invitation, no entry.' What do you do?
> **[A]** Try to persuade him you're on the list (Charisma + Subterfuge).
> **[B]** Attempt to intimidate him into letting you pass (Strength + Intimidation).
> **[C]** Look for another way in (Perception + Stealth).

## Key Components

- **`.roomodes`**: Contains the configuration for the `💀 WoD Storyteller (Interactive)` AI mode. This file is the "brain" of the AI, instructing it on the rules, the setting, and how to use the interactive workflow.
- **`character-sheet-wod-template.md`**: A template used by the AI to generate markdown character sheets for your characters.
- **`wod-quickstart-guide.md`**: A guide explaining the new WoD mechanics and how to interact with the Storyteller AI.
- **`campaigns/`**: This directory is where all your campaign-specific data will be stored by the AI, including character sheets and story notes. (Note: This directory is in `.gitignore` to prevent accidental commits of campaign data).

## Getting Started

1.  **Set up the MCP Servers**: Clone and configure the [Unified WoD MCP Servers](https://github.com/Mnehmos/rpg-mcp-servers) as per the instructions in their README. Ensure both the game-state and combat-engine servers are running.
2.  **Configure Roo Code**:
    - Ensure your Roo Code `mcp_settings.json` is correctly pointing to the running MCP servers.
    - Open this folder (`oWoD-Game-Experiment`) as your workspace root in VS Code. Roo Code will automatically detect and load the `storyteller-wod` mode from the `.roomodes` file.
3.  **Start a Chronicle**:
    - Activate the `💀 WoD Storyteller (Interactive)` mode in Roo Code.
    - Begin by telling the AI you want to create a character. It will guide you through the process step-by-step.
4.  **Play the Game**: Respond to the choices presented by the Storyteller to drive the narrative forward.
