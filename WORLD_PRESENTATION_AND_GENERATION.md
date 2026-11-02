# Pit Of Trials — World Presentation and Generation

**Status:** Working framework with the user's opening premise recorded as canon.  
**Purpose:** Define how to translate the user's story into a coherent, readable world and how to plan or generate its regions.  
**Canon rule:** Do not invent lore, history, factions, place names, world rules, or story events. When a needed fact is missing, mark it as an open question and continue only with presentation or layout work that does not depend on it.

## Worldbuilding workflow

When the user provides story material:

1. Extract only facts the user stated or clearly implied.
2. Keep a **Canon facts** list separate from **Visual interpretation** and **Open questions**.
3. Preserve the user's names, terminology, chronology, and cause-and-effect exactly.
4. Translate each story location and event into visual/environmental requirements without adding new explanation.
5. If two facts conflict, flag the conflict for the user rather than choosing one silently.
6. Update this document and the project design bible so they remain consistent.

## Story opening — canon supplied by the user

The world was inhabited by prehistoric monsters and creatures before a massive meteor struck. The meteor granted the world and its residents magic and abilities. Humankind began to evolve and rise, and life gathered around the enormous crater left by the impact. The crater has multiple levels; creatures become increasingly dangerous farther inside. The meteor broke into several pieces as it descended. Those pieces left behind ever-changing micro-dungeons on the levels. The dungeons behave as though alive and are never the same when entered. Each major level of the crater is a world of its own, with dangerous creatures and items to discover.

This is the opening premise, not a complete chronology or explanation. Do not add a cause for the meteor, define how humanity evolved, explain the crater's full nature, name any places or factions, or decide the origin of the living dungeons unless the user supplies or approves those facts.

### Short introductory synopsis

Before humanity rose, prehistoric creatures inhabited a world untouched by magic. Then a massive meteor struck. Its arrival changed the world and those who lived upon it, awakening magic and abilities across life itself. As humanity began to emerge, creatures and people alike gathered around the vast crater. Its depths descend through increasingly dangerous levels, each a world of its own. Scattered meteor fragments have left shifting micro-dungeons throughout the descent—living places that remake themselves with every entry. The crater promises rare discoveries and powerful items, but no expedition can rely on the same path twice.

This synopsis condenses the user's premise. It intentionally leaves the protagonist, first scene, conflicts, chronology details, and explanations for later story development.

### Story facts versus unanswered details

**Canon established:** prehistoric life predates the impact; a massive meteor struck; the meteor granted magic and abilities to the world and its residents; humanity began to evolve and rise afterward; life gathers around the impact crater; the crater has increasingly dangerous levels; the meteor broke into pieces while descending; fragments left ever-changing micro-dungeons; dungeons change between entries and feel alive; each crater level is a distinct world with dangerous creatures and items.

**Still open:** exact time spans; whether humanity was absent, rare, or simply not yet dominant before the impact; what "granted" means in different species; whether levels are vertical strata, enclosed regions, or both; how fragments create/change dungeons; why the dungeons feel alive; how settlements survive around the crater; and who the player is.

## Visual direction

The target presentation is fully 3D, colorful and stylized, viewed through an elevated three-quarter follow camera. The camera should keep the player, nearby creatures, interactable resources, and meaningful terrain readable at once. Use depth and perspective rather than a strict orthographic isometric projection unless a later direction changes this.

For the crater's overall feeling, the user points to *Made in Abyss*: a vast, layered descent where every depth feels like a distinct world, discovery inspires awe, and danger increases with depth. Treat this as a high-level mood and structure reference. Pit Of Trials must establish its own geography, inhabitants, imagery, palette, landmarks, and story expression; do not recreate specific scenes, characters, creature designs, or compositions from that work.

### Readability priorities

- Distinguish walkable ground, water, cliffs, hazards, and blocked routes by silhouette, value, color, and surface treatment.
- Keep creatures and gatherable objects legible against the terrain, especially from the default camera height.
- Use strong landmarks to communicate where the player is and where routes lead.
- Reserve the highest contrast and strongest effects for gameplay-relevant objects and story-directed moments.
- Make paths, gates, climb points, swim routes, and region transitions understandable from the play camera.
- Use stylized shapes and material detail that support the actual world described by the user; visual motifs must not imply unprovided lore.

### Reference use

- Check `E:\Game Ideas\Flora Assets` for plant and flora-related terrain references whenever designing vegetation, ground dressing, or biome-specific plant silhouettes. The current collection includes desert, lush forest, and tundra archives, and may expand.
- Check `E:\Game Ideas\Creature_Atlas_Next5_Families_Handoff\Creature_Atlas_Handoff` for creature identities and current bestiary scope. Its indexed count is changeable; consult its latest source before making a count claim or selecting canon species.
- Do not use content from `E:\Game Ideas\PrehistoricResources_v0.86.0_Build102` unless a clear overlap arises and the user first agrees to that reference.

## Region design sheet

Create one sheet for each story-approved region. Leave unknowns explicitly blank or marked `OPEN`; do not fill them with invented lore.

| Field | Notes |
| --- | --- |
| Region name | Use the user's name; otherwise `OPEN`. |
| Story purpose | Quote or summarize only the user's stated purpose. |
| Visual identity | Palette, silhouettes, materials, atmosphere, and key landmarks. |
| Terrain structure | Ground forms, elevation, water, traversal lanes, and boundaries. |
| Flora references | Exact archive folder/assets used, or `OPEN`. |
| Creature references | Exact atlas entries used, or `OPEN`. |
| Resources and interactions | Only those established or approved for this region. |
| Hazards and traversal | User-approved rules and how the player reads them visually. |
| Route connections | Entrances, exits, shortcuts, and progression gates. |
| Lighting and weather | Time-of-day/weather behavior if established. |
| Audio identity | Ambient layers and location cues; no lore-bearing additions without direction. |
| Gameplay landmarks | Distinct locations that aid orientation and navigation. |
| Open questions | Decisions that require the user's story or approval. |

## World layout and generation approach

The generation method is not a lore decision. The world has two scales: persistent crater levels that each function as a world, and smaller fragment-linked micro-dungeons that change between entries. Use a **designed macro layout with controlled variation** for persistent levels and a **recomposed, rule-bound layout** for micro-dungeons:

- Hand-place each level's world silhouette, major landmarks, story locations, entrances/exits, progression gates, and critical encounters. These levels form the stable geography players learn and return to.
- Design each crater level as a complete ecosystem and exploration space, not merely a corridor or dungeon floor. Its biome and visual identity must come from the user's story direction and reference collections.
- Build micro-dungeons from authored rooms, connectors, encounter spaces, reward spaces, and special set pieces. Assemble them differently for each entry while respecting connectivity, pacing, difficulty, and progression.
- Give each micro-dungeon a recorded identity/seed for its current expedition entry so it remains consistent while explored and can be reproduced for debugging. A later entry may generate a new valid configuration; persistence details remain open.
- Convey the "alive" impression through environmental behavior only as a proposal—such as shifting connections, changing room arrangements, or reactive ambience—until the user defines what living means in-world.
- Generate or vary supporting terrain, foliage placement, resource-node positions, ambient dressing, and low-risk encounters only inside authored constraints.
- Keep required routes, rewards, and interactions guaranteed; variation must not make a story beat, resource tier, or exit unreachable. Prevent unwinnable layouts and accidental soft locks.
- Prefer authored reusable chunks/rooms for caves, ruins, settlements, dungeons, or other spaces that need precise navigation or storytelling.
- For any procedural placement, define allowed surfaces, spacing, slope/water limits, biome tags, density ranges, and exclusion zones before placing assets.
- Use the current Flora Assets collection for flora choices. Match species and visual density to the approved region sheet; do not substitute invented plant designs where a reference exists.
- Use creature atlas IDs for creature spawns. Keep rarity, habitat, behavior, and encounter placement tied to approved creature data once those details are established.
- Keep placement reproducible with a recorded seed when randomness is used, so bugs and design feedback can be reproduced.
- Ensure generated dressing respects camera visibility, player navigation, combat arenas, interaction range, and performance budgets.

### Generation sequence

1. Read the user-approved story facts relevant to the crater level or dungeon.
2. For a persistent crater level, establish its authored boundary, traversable world space, landmarks, and connections to adjacent levels.
3. For a micro-dungeon, select a valid authored room set and generate a connected layout within bounds for size, length, difficulty, rewards, and exit placement.
4. Mark story-critical and gameplay-critical locations as fixed or guaranteed placements.
5. Assign terrain and biome tags to valid surfaces.
6. Place flora, resources, creatures, and ambient dressing from approved reference data within constraints.
7. Apply lighting, weather, atmosphere, and audio according to the region sheet.
8. Review from the three-quarter gameplay camera for readability, route clarity, and silhouette overlap.
9. Check that variation preserves required progression and that each generated layout's seed reproduces that entry.

## Open until the user defines them

- Further world history, factions, names, and terminology beyond the opening premise above
- What the title refers to within the story
- Crater level names, order, geography, and connections
- The reason the player explores and what progression means in-world
- Specific rules and limits of magic/abilities; hazards and supernatural effects
- How meteor fragments shape or affect the living micro-dungeons
- What "alive" means in the dungeons and what changes while the player is inside
- How much of each level is handcrafted versus generated
- Which level geography is permanent and what, if anything, changes between visits

## Story input record

Add user-provided story material here as it arrives. Preserve original wording for important canon statements.

### Canon facts

- Before the meteor, the world was inhabited by prehistoric monsters and creatures.
- A massive meteor struck and granted the world and its residents magic and abilities.
- Humanity began to evolve and rise after the impact.
- Life gathered around the enormous impact crater.
- The crater has multiple levels with increasingly dangerous creatures farther inside; each level is a world of its own, with dangerous creatures and items.
- The meteor broke into several pieces while descending. Its fragments left ever-changing micro-dungeons on the levels.
- Micro-dungeons feel alive and are never the same when entered.
- The desired reference for the crater's layered-world feeling is *Made in Abyss*, while Pit Of Trials retains original world and visual designs.

### Visual interpretation

- `OPEN — derive from user-provided canon`

### Open questions

- `OPEN — add only when a specific worldbuilding dependency needs clarification`
