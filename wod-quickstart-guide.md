# World of Darkness - Quickstart Guide

Welcome, Storyteller. This guide outlines how to use the MCP servers to run a World of Darkness chronicle.

## Character Creation

To create a new character, provide a detailed prompt to the AI.

> "I want to create a new character. A **Vampire** of the **Malkavian** clan. Their concept is a 'conspiracy-theorist hacker'. Let's give them high **Mental** attributes, focusing on Intelligence and Wits. For abilities, they should have high **Computer** and **Investigation**. Let's give them 3 dots in **Auspex** and 2 in **Dementation**."

The AI will use the `create_character` tool to build this character in the database.

## Making a Roll

All actions are resolved with dice pools. Simply state what your character is doing.

> "My character tries to sneak past the guard."

The Storyteller AI will determine the correct dice pool (e.g., Dexterity + Stealth), the difficulty, and use the `perform_roll` tool.

**Example Tool Call:** `perform_roll({ pool_size: 6, difficulty: 7, reason: "Dexterity + Stealth to sneak past guard" })`

The engine will return the number of successes or a botch, which the AI will then narrate.

## Combat

Combat is fast and deadly. A single `perform_combat_roll` handles an entire attack sequence.

> "The Brujah lashes out, trying to punch the security guard!"

The Storyteller AI calculates the pools and calls the tool:

**Example Tool Call:** `perform_combat_roll({ attacker_name: "Brujah Thug", defender_name: "Security Guard", attack_pool: 6, attack_difficulty: 6, damage_pool: 4, soak_pool: 3, damage_type: "bashing" })`

The engine will return a full summary: "The attack hits with 2 successes! They deal 3 levels of bashing damage, but the guard soaks 1. The guard suffers 2 levels of bashing damage." The AI then calls `inflict_damage` on the game-state server to record the result.

## Using Powers & Resources

State which power you are using. The AI will handle the rest.

> "I'm spending a point of Willpower to automatically succeed on this roll."

The AI calls: `spend_willpower({ character_id: 1 })`

> "My vampire is spending a blood point to increase their Strength."

The AI calls: `spend_resource({ character_id: 1, resource_name: "blood_pool", amount: 1 })` and then `update_character({ character_id: 1, updates: {"attributes.physical.strength": 5} })`

This system is designed to be narrative-first. Describe your intent, and the AI Storyteller will use the tools to resolve the mechanics.