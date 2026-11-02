# Pit Of Trials — Project Design Bible

**Project phase:** Brainstorming and organization  
**Engine:** Godot 4.7 project shell  
**Genre direction:** 3D action RPG, creature taming, gathering, crafting, farming, and life simulation  
**Camera direction:** Elevated three-quarter follow camera with a colorful stylized 3D presentation  
**Project status:** No gameplay systems have been built in this project yet.

This document is the working home for Pit Of Trials design decisions. It takes the interconnected hunt, tame, raise, craft, and explore loop of *Re:Legend* as a gameplay reference while keeping Pit Of Trials' world, story, characters, creature identities, art, and terminology original. The provided blueprints are planning inputs, not evidence that any feature already exists here.

## 1. Project pillars

1. **Hunt to progress:** Explore a dangerous frontier, learn creature behavior, and earn materials from encounters.
2. **Tame to build a team:** Befriend creatures with observation, food, and care; companions add combat and traversal options.
3. **Craft to reach farther:** Turn creature and environmental materials into better gear, tools, supplies, and access to more dangerous regions.
4. **Return to a home base:** Recover, care for the team, craft, farm, trade, and prepare for the next expedition.
5. **Make each expedition teach something:** New hazards, creature behaviors, resources, and routes give players reasons to adapt instead of only increasing numbers.

**Core loop:** Prepare at camp or settlement → choose an expedition goal → explore and gather → hunt, avoid, or befriend creatures → return with materials and discoveries → improve gear, companions, and home base → unlock a deeper route.

## 2. Design boundaries and source of truth

- **Creature canon:** Use `E:\Game Ideas\Creature_Atlas_Next5_Families_Handoff\Creature_Atlas_Handoff` for current and future creature concepts and bestiary planning. Its atlas currently states **171 indexed forms**; this is a working count and may change. The handoff identifies Clawberry (102–103), Rimecairn (104–105), Pitcherbit (106–108), Brontoth (109), and Velveleap (110–112) as prepared families whose portraits and turnarounds were not yet generated at handoff time. Check the latest atlas and handoff before using counts or production status.
- **Flora canon:** Use `E:\Game Ideas\Flora Assets` as the reference for flora and flora-related terrain assets. The current archive has desert, lush forest, and tundra collections; additions and revisions are expected. Inspect the relevant archive before choosing plants or making biome art.
- **Prior project:** `E:\Game Ideas\PrehistoricResources_v0.86.0_Build102` is out of scope by default. If a future Pit Of Trials feature clearly overlaps with it, pause that specific reuse and ask the user whether to consult/use the prior implementation. Do not silently import its assumptions or content.
- **Pasted blueprints:** Use the two supplied pasted texts as broad system checklists. Resolve contradictions in favor of the user's Pit Of Trials direction and current project-specific references. Mark uncertain mechanics as proposals, not facts about *Re:Legend*.
- **Originality:** Borrow broad genre structure and camera language only. Create original names, designs, writing, story, audio, and presentation assets.
- **Change tracking:** Creature totals, flora, regions, system scope, and progression values are provisional until explicitly locked by the user.

## 3. Brainstorm checklist

Use `[ ]` for unplanned, `[~]` for actively designed, and `[x]` only for an agreed design decision. These are planning items, not implementation-completion claims.

### Player and controls

- [ ] Character creation and appearance customization
- [ ] Elevated three-quarter 3D follow camera, fixed angle defaults, zoom options
- [ ] Movement, run, dodge, swim, interact, mount, and dismount
- [ ] Context targeting and clear action prompts
- [ ] Health, stamina, damage, fainting/defeat, recovery, and consequences
- [ ] Character attributes, levels, and activity-based progression
- [ ] Keyboard/mouse and controller mapping; accessibility options

### Combat and equipment

- [ ] Real-time melee, ranged, and supernatural/elemental combat direction
- [ ] Weapon families, combo identities, charged attacks, and signature abilities
- [ ] Enemy targeting, readable attack tells, hit response, and damage feedback
- [ ] Armor, accessories, resistances, equipment visuals, and upgrade rules
- [ ] Weapon mastery, status effects, and equipped skill/rune loadout
- [ ] Companion assistance and mounted combat
- [ ] Decide whether weapons are historically grounded, fantasy-inflected, or mixed

### Creatures and companions

- [ ] Discovery, habitat records, and in-game bestiary
- [ ] Taming interaction, preferred foods, and species temperament
- [ ] Trust, hunger, affection, grooming, rest, and recovery
- [ ] Creature levels, attributes, abilities, and battle roles
- [ ] Growth/evolution approach and any branching paths
- [ ] Breeding, fusion, rarity forms, and inherited traits (scope to decide)
- [ ] Mounts, traversal, and creature work abilities
- [ ] Active party, barns/storage, commands, naming, and companion limits
- [ ] Keep species identities and counts aligned with the current atlas

### Gathering, crafting, farming, and fishing

- [ ] Mining, logging, foraging, plant harvesting, and creature material collection
- [ ] Tool requirements, node states, respawn rules, and gathering proficiency
- [ ] Processing materials into components
- [ ] Recipes, workstations, quality outcomes, and crafting interactions/minigames
- [ ] Gear tiers, rarity, upgrades, enhancements, and repair/dismantling
- [ ] Cooking, food recipes, buffs, and consumable roles
- [ ] Planting, watering, fertilizing, crop stages, quality, seasons, and harvest
- [ ] Giant/special crops, underwater farming, and creature-assisted farm work
- [ ] Fishing catch loop, fish records, proficiency, habitats, time/weather variation
- [ ] Fish ponds/aquaculture, underwater exploration, and aquatic gathering
- [ ] Ground plant and terrain references in the Flora Assets collection

### Settlement and life simulation

- [ ] Shared clock, day/night, calendar, seasons, and weather
- [ ] Sleep, recovery, crop timing, and synchronized NPC/creature schedules
- [ ] NPC identities, dialogue, friendship, gifting, and personal quests
- [ ] Romance, marriage, festivals (decide whether and how these fit the tone)
- [ ] Shops, trading, currency, and economy
- [ ] Settlement restoration, construction, and upgrades
- [ ] Player housing, decoration, storage, and home customization

### Adventure and world

- [ ] Interconnected regions/biomes and their progression gates
- [ ] Main story, side quests, repeatable tasks, and quest journal
- [ ] Dungeons, enemy encounters, bosses, and expedition objectives
- [ ] Secrets, environmental puzzles, exploration rewards, and map/navigation
- [ ] Fast travel rules and unlock conditions
- [ ] Region-specific creature, flora, resource, hazard, and reward tables
- [ ] Decide the central mystery/conflict and what “deeper” means in the title

### Game infrastructure

- [ ] Inventory, equipment, storage, hotbar, and item comparison UI
- [ ] Character, skill, creature, crafting, farming, fishing, social, and map interfaces
- [ ] Manual/automatic saves and versioned save data
- [ ] Audio, music, animation, VFX, and readable interaction feedback
- [ ] Controller support and accessibility settings
- [ ] Single-player scope first; decide whether optional 1–4 player co-op is a later goal
- [ ] Performance targets, platform targets, testing approach, and build/version policy

## 4. Decisions to make before implementation

These are high-impact design questions. Keep them open until the user decides or the brainstorm has enough evidence to recommend a direction.

1. The opening premise is recorded in [WORLD_PRESENTATION_AND_GENERATION.md](WORLD_PRESENTATION_AND_GENERATION.md); why the player personally ventures deeper remains open.
2. What is the safe home base, and how does it change as the player advances?
3. What does defeating a creature mean in-world: harvesting, nonlethal capture, both, or species-specific outcomes?
4. Is taming mainly a trust/food interaction, a combat weakening loop, or a combination?
5. Are growth stages biological maturation, fantasy evolution, trained specialization, or a mixture by species?
6. What are the initial playable weapon families and the intended combat pace?
7. How many companions can accompany the player, and how much autonomy do they have?
8. Which life-simulation systems are central to the fantasy and which are optional expansion scope?
9. What are the first playable region and first meaningful equipment/creature milestones?
10. Is multiplayer a firm future requirement or simply an idea to revisit after a single-player prototype?

## 5. Recommended planning and production sequence

1. **Lock the pitch:** one-paragraph premise, pillars, target tone, and the meaning of the title.
2. **Define the first expedition:** home base, starter region, one resource loop, one combat encounter, one taming opportunity, and the return/reward beat.
3. **Map progression:** establish how creature materials, tools, armor, companion abilities, and region gates reinforce one another.
4. **Select initial content from canon:** consult the current creature atlas and relevant flora collection; record citations/IDs and unresolved details in content sheets.
5. **Write system briefs:** define player controls, combat, taming, inventory, crafting, time, and saving before expanding into festivals or multiplayer.
6. **Build a small playable slice:** only after the brainstorm is approved enough to guide implementation. Keep the slice data-driven and use original assets.
7. **Expand region by region:** add content only where it strengthens the hunt/tame/upgrade/explore loop.

## 6. Current project snapshot

- Godot project name: **Pit Of Trials**.
- Project configuration reports Godot feature version **4.7** and GL Compatibility rendering.
- The project currently contains the Godot shell and icon only; no gameplay implementation was found during this planning pass.
- This design bible is the initial organization artifact. No prior-project files or systems were imported.

## 7. Reference inputs

- World appearance, generation framework, and opening story canon: see [WORLD_PRESENTATION_AND_GENERATION.md](WORLD_PRESENTATION_AND_GENERATION.md). Follow the user's story and do not invent additional canon.

- User-provided `Complete Re:Legend-Style RPG Development Blueprint` pasted text: broad feature inventory, progression examples, and system ideas.
- User-provided `PREHISTORIC RESOURCES — MASTER GAME DEVELOPMENT SPECIFICATION` pasted text: Godot-oriented architecture and implementation checklist. Treat its instruction to audit/modify the old Prehistoric Resources project as inapplicable to this new Pit Of Trials shell.
- Creature reference handoff: `E:\Game Ideas\Creature_Atlas_Next5_Families_Handoff\Creature_Atlas_Handoff\README_HANDOFF.md`, `AGENTS.md`, atlas Markdown, and books/artwork as current references.
- Flora reference root: `E:\Game Ideas\Flora Assets`.
