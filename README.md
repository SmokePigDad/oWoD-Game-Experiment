# AI World of Darkness Experiment with Roo Code

This repository is the core client and AI logic for interactive, choice-driven World of Darkness chronicles powered by server-side rules. It defines all AI mode instructions, scene and sheet templates, and the client flow for immersive digital play—integrating fully with automated WoD backends that enforce every game mechanic.

---

## 🌙 What's New

- **Unified World of Darkness Coverage:** Supports Vampire, Werewolf, Mage, Changeling, Wraith, and Mummy with authentic tools for all supernatural archetypes (pre-Time of Judgment era only).
- **Choice Engine:** Implements the "Describe → Ask → Resolve" loop—AI narrates the scene, gives you meaningful choices, and all consequences are determined via backend servers enforcing the rules.
- **Stepwise Character Creation:** No more one-prompt sheets. The AI guides you through each attribute, ability, and background selection, and validates all choices against server-side WoD point-buy rules.
- **Visual Character Sheets:** Build and export HTML sheets and health trackers styled after the official books—directly from game state.
- **XP Menus:** Spend XP interactively, with the server checking all costs (attributes, powers, virtues, etc.).
- **Real-Time Resource Tracking:** All wounds, health, and resource stores (blood, rage, gnosis, glamour, etc.) are displayed with instant visual feedback, always reflecting current server state.
- **Server Integrity:** No calculations or fudge client-side—XP, wounds, power costs, and effects are always validated by the backend.
- **Crossover Play:** Any combo of supernaturals is valid for a single chronicle.

---

## 🕯️ The AI Storyteller Gameplay Loop

This client runs every chronicle using the explicit "Describe → Ask → Resolve" cycle:

1. **Describe:** AI sets the scene using real character/world data.
2. **Ask:** Player chooses from 3-5 explicit options—always phrased in character.
3. **Resolve:** AI calls the backend (`perform_roll`, `resolve_attack`, etc.) and narrates the outcome based on true server-validated results.

_Dice, powers, XP, wounds, and all mechanical effects are handled exclusively by MCP servers—AI never fudges or invents outcomes._

**Example:**
```
AI: The Ventrue Harpy eyes you coldly. "Do you truly serve the Camarilla, neonate?"
1. Lie your way through it (Manipulation + Subterfuge)
2. Assert dominance (Charisma + Leadership)
3. Use Presence to awe her
4. Remain silent and endure scrutiny
```
You choose; the AI resolves and narrates—servers enforce all rules behind the scenes.

---

## 🧩 Repository Structure

- **`.roomodes`:** Defines the 💀 WoD Storyteller (Interactive) mode and instructions.
- **`character-sheet-wod-template.md`:** Template for character sheets styled in official WoD "dots" format.
- **`wod-quickstart-guide.md`:** Brief rules summary and outline of interactive play.
- **`campaigns/`:** All campaign and character files are auto-generated here (not under version control).

---

## 🚀 Getting Started

1. **Set Up the [Unified WoD MCP Servers](https://github.com/SmokePigDad/rpg-mcp-servers):**
   - Clone, install, and start both `game-state-server` and `combat-engine-server`.
   - These enforce all dice, sheet, XP, power, and combat rules. No local fudge or math needed.

2. **Configure Roo Code:**
   - Connect both MCP servers by editing `mcp_settings.json`.
   - Open this directory as your VSCode workspace. Roo Code auto-detects and activates the `storyteller-wod` mode.

3. **Play a Chronicle:**
   - Start the 💀 WoD Storyteller mode in Roo Code.
   - Ask the AI to walk you through character creation, or begin your story and face the first dramatic choice.
   - Generate full HTML sheets and real-time health after every key event.

---

## ⚡ Key Features

- **Always Player-Driven:** AI never selects your action—all choices are up to you every step, every scene.
- **Full Rules Enforcement:** XP costs, wounds, powers, resources—all truly validated by the connected servers.
- **Visual Feedback:** Character sheets, health, and resource states are graphical and update after every significant action.
- **No Handwaving:** Every outcome is determined by the true Storyteller System rules—no homebrew or fudge.
- **Parity for PCs/NPCs:** All characters (PCs and NPCs) are controlled, tracked, and processed using the same server logic.

---

## ✨ Example Interactive Play

- **Scene Decisions:** Every action is presented as a choice with consequences. No railroading.
- **Combat:** Describe your tactic, make your choice; servers resolve the mechanics and AI narrates the results.
- **XP and Advancement:** Menus allow you to spend XP interactively—server checks all legality.
- **Campaign Logs:** AI maintains in-game chronicles and journals as the story develops.

---

**Start your own gothic-punk chronicle—where every choice is real, powers have weight, and WoD rules run behind every moment.**
