# Character Sheet: {{character_name}}

## Basic Information
- **Class**: {{character_class}}
- **Level**: {{level}}
- **Experience**: {{experience}} XP
- **Health**: {{current_hp}}/{{max_hp}}

## Attributes
| Attribute | Value |
|-----------|-------|
| Strength | {{strength}} |
| Dexterity | {{dexterity}} |
| Constitution | {{constitution}} |
| Intelligence | {{intelligence}} |
| Wisdom | {{wisdom}} |
| Charisma | {{charisma}} |

## Inventory
{{#inventory}}
- {{item_name}} ({{quantity}}) {{#equipped}}[EQUIPPED]{{/equipped}}
{{/inventory}}

## Story Progress
- **Current Chapter**: {{current_chapter}}
- **Current Scene**: {{current_scene}}
- **Achievements**: {{#achievements}}- {{.}} {{/achievements}}