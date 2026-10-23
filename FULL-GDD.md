# Master Builders VR - FULL GDD - Complete Complex Version with All Integrations

**Full Vision by Pedro Simental Jacinto - Guaymas, Sonora, Mexico**
**For Reference: MVP 0.1 is only in README.md. This is the full roadmap Phase 0.2 to Phase 4.**

This document contains the complete, complex, integrated design. Not for first production run. This is the studio roadmap.

---

## 1. CORE PILLAR: "The Game Validates, Classifies, and Evaluates"

**No Recipes. You build it with your hands in VR. The game decides what it is, what it can be, and who you become.**

### The 3-Layer Integrated System

#### Layer 1: Material Layer - Deterministic & Fixed (Database)

Every material has fixed, non-negotiable stats. No RNG.

| Material | Edge | Durability | Weight | Heat Resist | Soul Affinity |
|----------|------|------------|--------|-------------|---------------|
| Banana Leaf | 0 | 1 | 0.1 | 0 | Nature |
| Pine Wood | 5 | 15 | 2.0 | 5 | Neutral |
| Oak Wood | 12 | 40 | 4.5 | 15 | Neutral |
| Boar Bone | 18 | 30 | 3.0 | 10 | Beast |
| Black Iron | 50 | 100 | 8.0 | 80 | Fire, Dark |
| Mythril (Legendary) | 90 | 200 | 3.5 | 200 | All |

*   Compatibility Rule: Fire Soul cannot be bound to Banana Leaf (10 heat resist vs 100 fire soul = item burns). Game auto-degrades to Ash Decoration.

#### Layer 2: Form Layer - Structural Validation (The Magic Moment)

**Game doesn't invent. Game VALIDATES based on structural tags.**

Validation Algorithm (Fair, not fuzzy):

*   **Sword Check:** `blade_length >= grip_length * 2.5` + `center_of_mass < 0.4 from grip` + `2 attachment points (blade-grip)` + `edge > 0`
*   **Axe Check:** `head_weight > handle_weight * 1.5` + `support_count >= 2` + `blunt > 10`
*   **Invalid Object:** Becomes **Decoration** by design. Player becomes `Decorator +`. Not punishment, identity. Decorators have higher trade value with NPC nobles.

**If Valid, Game Classifies:**
- Class: Sword, Axe, Hammer, Spear, Shield, Furniture, Tool, Decoration
- Quality Tier: Trash / Common / Fine / Masterwork / Legendary (based on symmetry, ratio accuracy)
- Legal Stat Range: A Wooden Sword can NEVER have 100 edge, even with Legendary Soul. Capped by Material + Form.

#### Layer 3: Soul Layer - Personality by Accumulation (The Heart of the Game)

Souls are NOT craftable. Souls are hunted. Souls have identity.

**Soul Types & Behavior Change (Not just stats):**

*   **Boar Soul:** +Strength, +Intimidation, +Beast Attraction. Weapon grunts when near boars. 10 souls = All beasts in 50m know where you are.
*   **Rabbit Soul:** +Swiftness, +Silent Movement, +Dodge. Weapon vibrates when danger near.
*   **Wolf Soul:** +Tracking, +Pack Presence, +Night Vision. Howls when wolves nearby. Stacking 5+ wolves makes other wolves non-hostile, but villagers fear you.
*   **Guardian Soul (Rare):** +Protection Aura, +Reputation with villages, -Mobility. Weapon glows near sacred places.
*   **Sleeping Beast Soul (Legendary - 4 total in world):** World-changing behavior. One Beast was the one that destroyed your home country.

**Strict Rules to Prevent Infinite Stacking (Balance):**

1.  **Max Soul Count:** 10 total per item. MVP Test: 3 max.
2.  **Diminishing Returns:** Soul 1 = 100%, Soul 2 = 70%, Soul 3 = 45%, Soul 10 = 5%
3.  **Affinity Rules:** Fire Soul on Ice Material = -50% power + smoke particle + reputation loss with Ice Village
4.  **Incompatibility Penalty:** Boar + Rabbit = Conflicted Personality - weapon randomly bucks (10% chance to miss). Requires Shaman NPC to purify.
5.  **Class Caps:** Beginner Sword can hold max 3 souls. Master Sword can hold 10. Forces progression.
6.  **Degrading Behavior Over Time:** Souls fade if not fed. Feed with same beast essence or item becomes Cursed (negative stats).
7.  **Visibility / Risk Tradeoff:** `Risk = Souls^2 * Rarity`. 10 Boar Souls = Beacon on map. Everyone knows where you are, including other players and beasts.

**Formula Final:**
`Final Power = ((Material Base + Form Quality Bonus) * (1 + Sum_Diminished_Souls)) * Rarity_Multiplier`
`Capped by: Material Max * Form Max * Soul Cap`

**Identity Loop:** `You Are What You Build + What Souls You Find + How Villagers Remember You`

---

## 2. FULL INTEGRATIONS - Persistent World Systems

### A. Economy & Reputation Integration

*   **No Global Auction House.** Physical trade only. You hand the item in VR.
*   **NPC Economy 24/7 (Phase 2+):** Each NPC has needs, gold, daily routine. Baker needs flour daily. If you flood market with swords, price crashes 70% for 3 days.
*   **Social Reputation:**
    - Build too many Boar Soul weapons = Title: "The Boar Caller" - Villagers lock doors, hunters respect you, beasts hunt you.
    - 10 Rabbit Soul items = "The Silent One" - Can enter noble houses, but guards don't see you (good and bad).
    - Reputation locked to village. New village doesn't know you.
*   **Profession Branching (Locked):** 
    - Nomad - / Nomad / Nomad + / Nomad ++ / Nomad +++
    - -> Blacksmith - / + / ++ / +++ (Requires Village Anvil)
    - -> Carpenter - / + / ++ / +++ (Requires Sawmill)
    - -> Hunter - / + / ++ / +++ (Requires Wilderness survival 7 days)
    - -> Cook, Shaman, Decorator, Guardian (Phase 3+)
    - You cannot be Blacksmith +++ and Hunter +++. Choosing closes branches. Forces identity.

### B. Building / Housing - Sacred 4x4 Hut System

*   **Base Hut:** 4x4 sacred space. Only you can build inside. No griefing.
*   **Rules:** Hut must have 4 walls, roof, door, fire. Game validates like weapons. If invalid, collapses.
*   **Upgrade:** 4x4 -> 8x8 (Requires Carpenter + and Village reputation 50+)
*   **Soul Bound Hut:** Put Guardian Soul in central pillar = Protection Aura, items inside don't degrade. Put Boar Soul = Hut attracts boars to farm.

### C. Combat Integration

*   **One Combat Loop (MVP):** Physical swing, block with object, weight matters. Heavy hammer = slow but breaks guard.
*   **Soul Combat:** Wolf Soul sword tracks bleeding enemy for 10s (visible scent trail in VR).
*   **Death:** You drop 1 random soul from your weapon. Other player can loot it. High risk for high soul count.

### D. Temporary Dungeons (Phase 2) - 1 Week Rotation

*   Dungeons appear for 1 week, anywhere. Inside: rare materials + rare souls.
*   **Soul Accumulation Mechanic:** The more players enter with same Soul type, dungeon mutates. 10 players with Boar Souls enter = Dungeon becomes Boar Nest, final boss is Boar Mother with 10x HP but drops Boar King Soul (Legendary).
*   **Closes after 1 week.** If not cleared, collapses and becomes rich mine for materials.

### E. Global Boss Secrets - The 4 Sleeping Legendary Beasts

*   **4 Beasts, 1 per quadrant, hidden, sleeping. Not marked on map.**
*   One of them destroyed your home country (your lore start).
*   **How to find:** Collect 100 souls of its type, weapon whispers direction. Or find 4 ancient map pieces in dungeons.
*   **Mechanics:** Cannot be killed alone. Requires 20+ players with high-tier soul weapons. If awakened, Beast walks persistent world for 3 real days, destroying villages. If killed, drops its Legendary Soul. Its Soul allows you to build Legendary class items (Mythril tier). Only 1 player per server can hold a Legendary Beast Soul at a time.
*   **World Impact:** If all 4 Beasts are killed in one month, server enters "Age of Builders" - all building is 2x faster for 1 week.

### F. Persistent World Systems

*   **Shard System:** 1 village = 1 shard = 10-20 players max. No 1000 player lag. Villages connect via nomad roads.
*   **Time:** Real time. 1 day real = 1 day game. Night is dark, need torch (Pine Wood + Fire Soul).
*   **Seasons:** 7 real days = 1 season. Winter: no banana leaves, boars hide, wolves stronger.

---

## 3. MVP vs FULL - Clarity

| Feature | MVP 0.1 (README.md) | FULL (This Document) |
|---------|---------------------|----------------------|
| Map | 1 hill, 200 trees, 20 animals | 4 quadrants, 10000+ trees, 4 beasts |
| Level Cap | Nomad Lvl 2 max | Master +++ (Lvl 5) |
| Branches | 3 branches, only - and no sign | All 7 branches to +++ |
| Soul Max | 3 souls max | 10 souls max, Legendary Souls |
| NPCs | None | 24/7 economy, 50+ NPCs per village |
| Building | No | Sacred 4x4 Hut System |
| Dungeons | No | Temporary 1-week rotation |
| Bosses | No | 4 Sleeping Legendary Beasts (world event) |

---

## 4. Why This Is Balanceable

Despite complexity, core is deterministic:

1.  Material Fixed + Form Validation = No exploit. You cannot make Mythril sword from leaves.
2.  Soul Diminishing + Risk Tradeoff = No infinite power. More power = more visibility = more danger.
3.  Class Caps + Profession Locks = No jack-of-all-trades. Forces social economy (need other players).
4.  Physical Trade + Shard Size = Economy cannot be crashed by bots.

---

## 5. Tech Stack for Implementation

*   VR: Unity XR + OpenXR + FinalIK (hand building)
*   Validation: Custom C# rule engine (tags and ratios)
*   Persistence: Fish-Net + PlayFab (shards)
*   Voice: "You are a Blacksmith -" using TTS local

This GDD is for reference and progressive implementation. Start with README.md.

---
*If you read this far, you understand: Start small (Nomad Refugee), build to legendary (Beast Slayer).*

