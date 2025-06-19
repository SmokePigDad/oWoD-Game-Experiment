# World of Darkness Character Record

## I. Vitals
- **Name:** {{name}}
- **Concept:** {{concept}}
- **Nature:** {{nature}}
- **Demeanor:** {{demeanor}}
- **Character Type:** {{character_type}}
- **Primary Splat:** {{splat1}}
- **Secondary Splat:** {{splat2}}

---
## II. Attributes
*A dot (•) represents one level in a Trait.*

| Physical | Rating | Social | Rating | Mental | Rating |
|:---|:---:|:---|:---:|:---|:---:|
| Strength | {{'•' * attributes.physical.strength}} | Charisma | {{'•' * attributes.social.charisma}} | Perception | {{'•' * attributes.mental.perception}} |
| Dexterity | {{'•' * attributes.physical.dexterity}} | Manipulation | {{'•' * attributes.social.manipulation}} | Intelligence| {{'•' * attributes.mental.intelligence}}|
| Stamina | {{'•' * attributes.physical.stamina}} | Appearance | {{'•' * attributes.social.appearance}} | Wits | {{'•' * attributes.mental.wits}} |

---
## III. Abilities
| Talents | Rating | Skills | Rating | Knowledges | Rating |
|:---|:---:|:---|:---:|:---|:---:|
| Alertness | {{'•' * abilities.talents.alertness}} | Animal Ken | {{'•' * abilities.skills.animal_ken}} | Academics | {{'•' * abilities.knowledges.academics}} |
| Athletics | {{'•' * abilities.talents.athletics}} | Drive | {{'•' * abilities.skills.drive}} | Computer | {{'•' * abilities.knowledges.computer}} |
| Brawl | {{'•' * abilities.talents.brawl}} | Etiquette | {{'•' * abilities.skills.etiquette}} | Finance | {{'•' * abilities.knowledges.finance}} |
| Dodge | {{'•' * abilities.talents.dodge}} | Firearms | {{'•' * abilities.skills.firearms}} | Investigation| {{'•' * abilities.knowledges.investigation}}|
| Empathy | {{'•' * abilities.talents.empathy}} | Melee | {{'•' * abilities.skills.melee}} | Law | {{'•' * abilities.knowledges.law}} |
| Intimidation| {{'•' * abilities.talents.intimidation}}| Performance | {{'•' * abilities.skills.performance}} | Linguistics | {{'•' * abilities.knowledges.linguistics}}|
| Leadership | {{'•' * abilities.talents.leadership}} | Stealth | {{'•' * abilities.skills.stealth}} | Medicine | {{'•' * abilities.knowledges.medicine}} |
| Streetwise | {{'•' * abilities.talents.streetwise}}| Survival | {{'•' * abilities.skills.survival}} | Occult | {{'•' * abilities.knowledges.occult}} |
| Subterfuge | {{'•' * abilities.talents.subterfuge}}| Larceny | {{'•' * abilities.skills.larceny}} | Politics | {{'•' * abilities.knowledges.politics}} |

---
## IV. Advantages
| Backgrounds | Rating | Powers | Rating |
|:---|:---:|:---|:---:|
{% for name, value in backgrounds.items() %}
| {{name}} | {{'•' * value}} |
{% endfor %}
| | |
{% for power_type, powers_list in powers.items() %}
| **{{power_type.title()}}** | |
{% for name, value in powers_list.items() %}
| *{{name}}* | {{'•' * value}} |
{% endfor %}
{% endfor %}

---
## V. Traits & Resources
| Virtues / Traits | Rating | Resources | Current / Max |
|:---|:---:|:---|:---:|
{% for name, value in virtues_or_traits.items() %}
| {{name.title()}} | {{'•' * value}} |
{% endfor %}
| | |
| Willpower | {{'•' * willpower_current}} / {{'•' * willpower_permanent}} |
{% for name, value in resources.items() %}
| {{name.title()}} | {{value}} |
{% endfor %}

---
## VI. Health
*Mark damage from left to right. [ / ] Bashing, [ X ] Lethal, [ * ] Aggravated*

| Health Level | Penalty | Boxes |
|:---|:---:|:---:|
| Bruised | +0 | [ ] |
| Hurt | -1 | [ ] |
| Hurt | -1 | [ ] |
| Wounded | -2 | [ ] |
| Wounded | -2 | [ ] |
| Mauled | -5 | [ ] |
| Crippled | -5 | [ ] |
| Incapacitated | unconscious | [ ] |

**Current Wound Penalty:** {{wound_penalty}}