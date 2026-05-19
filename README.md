# Wash Towel Fill – Big Game Design Document
![Cover Image of Cheescake and Beefcake](https://i.imgur.com/gTym87U.png)

> **Working title:** Wash Towel Fill  
> **Abbreviation:** WTF  
> **Core design pillar:** WTF is a **Big Game**.  
> **Primary platform:** Web browser, desktop and mobile  
> **Target domain:** `washtowelfill.io`  
> **Legacy location:** `silverwaregames.com/games/wtf/`  
> **Status:** Active design / multiplayer direction rewrite

# One-Sentence Pitch

**Wash Towel Fill is a browser-based, persistent multiplayer tower-wars car-wash game where every player joins one of three ridiculous 24/7 car-wash factions, helping their boss clean cars, send dirty waves, fight rival washes, and keep the whole city from drowning in grime.**

# High Concept

The original idea for WTF was a multiplayer tower-defense / tower-wars game where each player owns a personal car wash, places wash equipment and staff along a path, and sends waves of cars to other players.

This revision keeps the best parts of that idea:

- Browser-based play
- Tower-defense / tower-wars strategy
- Car-wash humor
- Sending waves of cars
- Team-based progression
- Backend-driven multiplayer
- Short-session accessibility
- Beefcake and cheesecake energy

But the multiplayer structure changes.

Instead of every player owning a private car wash, the server owns **three permanent faction car washes** that exist all the time, like persistent bases on a Minecraft server.

Players log in, choose a boss/faction, and contribute to an ongoing shared wash.

The game is not just:

> “My car wash versus your car wash.”

It is:

> **“Our ridiculous car wash versus their ridiculous car wash, while the entire city gets dirtier around us.”**

# The Big Game Principle

WTF should be designed as a **Big Game**.

A Big Game is a multiplayer game where:

- The play space is shared.
- The world keeps existing when one player logs off.
- Casual players can help meaningfully in seconds.
- Hardcore players can organize, optimize, and lead.
- Players feel like they are part of something larger than their individual session.
- Competition creates drama, but the game prevents one group from ruining the fun for everyone else.

The guiding slogan:

> **Everyone gets wet. Nobody gets drowned.**

That means WTF should be chaotic, social, competitive, silly, and sometimes unfair in a funny way — but never hostile, hopeless, or dominated by a small handful of players forever.

# Design Goals

## 1. Easy to join, hard to master

A new player should be able to log in, pick a boss, click a few useful buttons, laugh, and leave having helped.

A committed player should be able to spend hours studying layouts, timing waves, proposing upgrades, and organizing faction strategy.

## 2. Persistent faction identity

The player should feel like they work for a strange, charismatic car-wash empire.

They are not just choosing “red team / blue team / green team.”

They are choosing a boss, a brand, a culture, and a running joke.

## 3. Competitive and collaborative pressure

The three factions compete for seasonal dominance.

At the same time, all three factions are threatened by a shared city-wide dirt problem: **The Grime**.

If players only attack each other and ignore the shared threat, everyone suffers.

## 4. Backend authority

WTF is intended to be Silverware Games’ first title with proper backend multiplayer logic.

The client should be a renderer and input layer.

The backend should be the source of truth.

The backend validates actions, owns faction state, simulates waves, resolves tower behavior, prevents cheating, records logs, and broadcasts updates.

## 5. No private-base loneliness

Private bases can make players feel isolated.

The Big Game model turns every contribution into public faction progress.

Even a small action should feel like it moved the shared machine forward.

# The Three Permanent Car Washes

The server runs three persistent car washes.

Each wash has:

- A faction boss
- A permanent layout
- Shared upgrades
- A faction treasury
- A seasonal score
- A public action log
- Current incoming waves
- Current outgoing attacks
- Maintenance state
- Faction-specific bonuses
- Faction-specific jokes, cosmetics, and flavor

Players choose which wash they currently work for.

# Faction 1: The Beefcakes

## Boss

**Chaz “The Shammy” Thunderbuff**

A wildly positive speedo-wearing car-wash bodybuilder who believes every problem can be solved with enough foam, flexing, and deltoid confidence.

He is not mean. He is not macho in a cruel way. He is a himbo motivational poster with a pressure washer.

## Personality

- Loud
- Physical
- Direct
- Encouraging
- Overconfident
- Weirdly wholesome

## Faction Fantasy

The Beefcakes are the faction for players who want to smash through problems with raw wash power.

They believe in throughput, strength, burst cleaning, and huge visible results.

## Gameplay Identity

The Beefcakes should be:

- Strong at early and mid-wave cleaning
- Good at raw dirt removal
- Good at burst effects
- Good at recovering from messy waves
- Less efficient if poorly coordinated
- More likely to waste resources through overkill

## Example Bonuses

- Brush Stations gain bonus power during “Flex Rush.”
- Towers temporarily fire faster after a successful defense.
- Failed waves still generate some “Motivation” resource.
- Heavy vehicles are cleaned more effectively.

## Sample Slogans

- “We don’t rinse. We dominate.”
- “No grime survives leg day.”
- “Suds out, guns out.”

# Faction 2: The Cheescakes

> Naming note: “Cheescakes” preserves the existing WTF/cover-image gag spelling. The final spelling can be standardized later if needed.

## Boss

**Cherry Suds Valentine**

A glamorous, retro, over-the-top car-wash diva who treats each wash cycle like a stage performance.

She is not just “sexy lady faction.” She is the theatrical queen of clean: polished, dramatic, competitive, and terrifyingly competent.

## Personality

- Stylish
- Precise
- Dramatic
- Competitive
- Elegant
- Ruthless about presentation

## Faction Fantasy

The Cheescakes are the faction for players who want to win through coordination, multipliers, timing, and clean streaks.

They turn washing into performance.

## Gameplay Identity

The Cheescakes should be:

- Strong at score multipliers
- Strong at customer happiness
- Strong at combo chains
- Strong at upgrade efficiency
- More dependent on proper sequencing
- More vulnerable to messy disruption

## Example Bonuses

- Wax Applicators generate stronger score multipliers.
- Clean streaks build “Glamour.”
- Well-timed towers grant bonus customer tips.
- Luxury cars generate extra rewards when fully cleaned.

## Sample Slogans

- “Cleanliness is glamour.”
- “Every rinse deserves a spotlight.”
- “A perfect finish is never accidental.”

# Faction 3: The Spacecakes

## Boss

**Mx. Squeegee Prime**

A many-limbed alien / robot / soap-being from beyond human marketing categories.

The first two factions are comically gender-coded. The Spacecakes are the joke that breaks the binary without making nonbinary people the punchline.

Mx. Squeegee Prime is not “the weird gender joke.”

They are the cosmic chaos option.

Their view of the Beefcakes and Cheescakes:

> “Your primitive two-cake taxonomy is adorable.”

## Personality

- Strange
- Analytical
- Alien
- Deadpan
- Adaptive
- Unsettlingly efficient

## Faction Fantasy

The Spacecakes are for players who like weird systems, strange synergies, reconfiguration, and controlled chaos.

They do not simply clean cars.

They revise the assumptions under which cars become clean.

## Gameplay Identity

The Spacecakes should be:

- Strong at adaptation
- Strong at tower mutation
- Strong at route manipulation
- Strong at strange combo effects
- Harder for new players to understand
- Powerful when coordinated by skilled players

## Example Bonuses

- Towers can temporarily mutate into alternate functions.
- Certain paths can be rerouted or phase-shifted.
- Weird cars produce special resources.
- Failed defenses may generate experimental data instead of pure loss.

## Sample Slogans

- “All forms shall be rinsed.”
- “Dirt is a local superstition.”
- “The foam remembers.”

# Player Identity

Players do not simply pick a team.

They choose who they work for.

Possible player titles:

- Beefcakes Intern
- Beefcakes Shift Lead
- Cheescakes Floor Manager
- Cheescakes Glam Technician
- Spacecakes Foam Adept
- Spacecakes Reality Squeegee
- Freelance Sponge
- Unionized Towel Goblin

Titles should be funny, visible, and tied to faction loyalty, contribution, or seasonal role.

# Core Gameplay Loop

1. Player visits WTF in the browser.
2. Player logs in or plays as a temporary guest.
3. Player chooses a boss/faction.
4. Player sees the current state of the three car washes.
5. Player takes one or more useful actions:
   - Scrub
   - Repair
   - Donate
   - Vote
   - Send a wave
   - Upgrade a tower
   - Propose a layout change
   - Help defend an incoming wave
6. The server validates the action.
7. The shared faction state updates.
8. Other players see the change.
9. The faction earns progress, score, resources, or trouble.
10. The larger server story continues.

# Session Length Targets

WTF should support multiple levels of commitment.

## 30-Second Player

A casual player can:

- Pick a faction
- Claim a daily shift
- Click “Scrub Rush”
- Repair a broken tower
- Vote on the next upgrade
- Donate soap/towels/currency
- Cheer for the boss
- Collect a small reward

The 30-second player should not need to understand pathing, wave math, tower ranges, or faction politics.

## 3–5 Minute Player

A short-session player can:

- Help defend a wave
- Send a small car wave
- Upgrade a tower
- Complete a mini-objective
- Review faction goals
- Vote on proposals
- Check the leaderboard

## 30+ Minute Player

A hardcore player can:

- Study layouts
- Optimize tower placement
- Time coordinated attacks
- Manage resource spending
- Propose structural changes
- Lead faction chat
- Analyze rival weaknesses
- Prepare for server events
- Maintain strategy guides
- Act as a faction foreman or architect

# Core Systems

## 1. Persistent Faction Washes

Each faction wash is a shared board.

The board includes:

- Path layout
- Tower slots
- Towers placed
- Tower levels
- Active buffs/debuffs
- Incoming cars
- Current wave status
- Maintenance problems
- Treasury
- Faction upgrades
- Action log
- Proposal queue
- Seasonal stats

The server should persist this state in a database.

The car washes should continue to exist even when no players are online.

Whether they continue simulating in real time or advance in scheduled ticks is an implementation decision.

## 2. Towers / Wash Stages

Towers represent car-wash equipment, workers, and absurd wash technology.

Existing tower concepts to preserve:

### Brush Station

- Removes heavy dirt
- Slow but powerful
- Good against muddy or heavily soiled vehicles

### Spray Hose

- Medium dirt removal
- Faster throughput
- Reliable general-purpose tower

### Wax Applicator

- Adds score multipliers
- Improves final value of successfully cleaned cars
- Works best when combined with other stages

### Dryer Station

- Finalizes the clean
- Converts cleanliness into score
- May affect customer happiness or finish quality

### Additional Possible Towers

#### Vacuum Goblin

- Removes interior mess
- Strong against family vans, taxis, and snack-covered cars

#### Foam Cannon

- Area effect
- Covers multiple cars
- Can create visibility chaos

#### Buff Towel Crew

- Boosts nearby towers
- Repairs tower wear over time

#### Tip Jar Shrine

- Converts customer happiness into faction currency
- Weak direct cleaning but strong economy

#### Reality Rinse Gate

- Spacecakes-flavored tower
- Mutates or reorders wash stages temporarily

## 3. Cars / Enemy Units

Cars are the units that move through car-wash paths.

Existing car concepts to preserve:

### Old Rusty Car

- High dirt
- Slow
- Tough but predictable

### Muddy Truck

- Resistant to early cleaning
- Requires strong dirt removal

### Luxury Sedan

- Lower dirt
- High score potential
- Punishes sloppy finishing

### Fleet Vehicles

- Arrive in groups
- Test throughput and path efficiency

### Additional Possible Cars

#### Snack Van

- Drops interior mess
- Strong against exterior-only builds

#### Pollen Coupe

- Applies recurring grime if not cleaned quickly

#### Bird-Bombed Convertible

- Requires special treatment
- Gross but high comedy value

#### Influencer SUV

- High reward if perfectly cleaned
- Large penalty if customer happiness is low

#### Haunted Hearse

- Seasonal event car
- Weird status effects

## 4. Sending Waves

Players can send dirty cars against rival faction washes.

This preserves the tower-wars offense/defense idea while adapting it to the three-faction model.

### Wave Goals

Sending a wave should:

- Help the sender’s faction
- Pressure a rival faction
- Create visible drama
- Give defenders something to rally around
- Feed the server-wide story

### Wave Rules

A wave should have:

- Cost
- Cooldown
- Target faction
- Car composition
- Difficulty rating
- Expected reward
- Risk/reward profile
- Visibility in the public action log

### Example Wave Types

#### Mud Rush

A simple wave of muddy cars.

#### Luxury Panic

A wave of high-value cars that punish sloppy finishing.

#### Fleet Flood

A large number of medium-difficulty vehicles.

#### Bird Poop Ambush

Gross comedy wave with special cleaning requirements.

#### Rival Influencer Inspection

A dangerous wave that affects public reputation if failed.

## 5. Defense

When a faction is attacked, players can help defend.

Defense actions should support both casual and hardcore players.

### Casual Defense Actions

- Scrub Rush
- Temporary foam boost
- Repair a damaged tower
- Cheer for a worker
- Activate boss catchphrase
- Donate emergency towels

### Hardcore Defense Actions

- Adjust tower targeting
- Reassign tower priorities
- Trigger saved defensive plans
- Propose layout changes
- Coordinate timing with other players
- Spend treasury on emergency upgrades

## 6. The Grime Meter

The Grime Meter is the shared world threat.

All three factions compete, but the city itself is getting dirtier.

If the Grime Meter rises too high, everyone suffers.

### Grime Sources

- Failed car washes
- Overuse of dirty attack waves
- Server events
- Neglected maintenance
- Rival sabotage
- Seasonal disasters

### Grime Consequences

If Grime gets too high:

- Cars arrive dirtier
- Customer happiness drops
- Rewards decrease
- Health Inspector events trigger
- More maintenance problems appear
- All factions suffer penalties

### Grime Reduction

Factions reduce Grime by:

- Cleaning cars well
- Completing public events
- Cooperating during emergencies
- Donating to shared cleanup drives
- Temporarily pausing attacks during disasters
- Completing city-wide objectives

### Design Purpose

The Grime Meter creates collaboration inside competition.

Players should ask:

> “Can we beat the other washes without destroying the whole city?”

## 7. Faction Progression

Each faction has shared progression.

Possible progression categories:

- Cleaning Power
- Throughput
- Customer Happiness
- Treasury Efficiency
- Defensive Tools
- Offensive Wave Options
- Cosmetic Branding
- Boss Abilities
- Emergency Responses
- Special Event Unlocks

Faction progression should be visible and emotionally satisfying.

Players should feel proud when their faction unlocks something.

## 8. Personal Progression

Players should also have personal progression, but it must not undermine the Big Game.

A player can earn:

- Account level
- Titles
- Cosmetics
- Profile badges
- Seasonal trophies
- Boss affinity
- Contribution history
- Voting weight modifiers
- Access to trusted roles

Personal progression should reward participation without letting one player dominate the shared state.

## 9. Switching Factions

Players should be able to switch factions, but the rules need to prevent abuse.

This action should be framed in-world as:

- Transfer paperwork
- Defection
- Changing shifts
- Being recruited
- Joining a rival wash

### Recommended Rule

Players may switch factions, but:

- They keep personal account progress.
- They keep cosmetics.
- They keep general unlocks.
- They lose or reduce current faction loyalty bonuses.
- They may have a cooldown before switching again.
- Their new faction receives a public “new hire” announcement.

### Seasonal Transfer Windows

During certain windows, transfers can be free or cheaper.

Outside those windows, switching costs currency, loyalty, or time.

### Why Allow Switching?

Switching lets players:

- Join friends
- Escape a dead faction
- Balance population
- Roleplay betrayal
- Explore different play styles

### Why Restrict Switching?

Restrictions prevent:

- Bandwagoning to the winning faction
- Scouting abuse
- Economic exploitation
- Last-minute seasonal score manipulation

## 10. Roles, Trust, and Anti-Griefing

Persistent shared bases require protection.

One troll should not be able to destroy a faction’s car wash.

### Role Ladder

#### Visitor

- Can observe
- Can perform limited casual actions
- Can pick a faction

#### Worker

- Can contribute resources
- Can join defenses
- Can vote
- Can send basic waves

#### Trusted Worker

- Can propose layout changes
- Can place temporary objects
- Can spend limited faction resources

#### Foreman

- Can approve certain proposals
- Can manage defensive plans
- Can spend larger amounts of treasury

#### Architect

- Can modify major layout systems
- Can prepare saved build plans
- Can organize faction infrastructure

#### Boss Council / System Authority

- Final protection layer
- Major destructive changes require votes, cooldowns, or automated checks

### Action Logs

Every meaningful action should be logged.

Examples:

- `FoamLord97 upgraded Brush Station B4 to Level 3.`
- `CherryFan88 sent Luxury Panic against The Beefcakes.`
- `SqueegeeScholar moved Dryer Station from C2 to C4.`
- `The Spacecakes voted to mutate the east tunnel.`
- `The Beefcakes failed to stop a Mud Rush. Grime +4.`

Logs make the world feel alive and make griefing easier to detect.

### Anti-Griefing Rules

The server should prevent:

- Selling all towers at once
- Spending the entire treasury without permission
- Blocking all paths
- Creating unwinnable layouts
- Spamming waves too quickly
- Switching factions repeatedly for abuse
- Coordinated harassment of a low-population faction

## 11. Layout and Pathing

The old design includes cars pathfinding through a car wash.

That should remain important.

### Pathing Goals

- Easy to read
- Hard to optimize perfectly
- Supports tower-defense strategy
- Supports faction identity
- Allows visual comedy
- Prevents grief layouts

### Path Rules

Possible rules:

- Cars must always have a valid route from entrance to exit.
- The server validates layout changes before accepting them.
- Build slots may be fixed, semi-fixed, or modular.
- Certain advanced roles can propose path changes.
- Emergency events may temporarily alter paths.
- Factions can save and vote on layout plans.

### Anti-Block Rule

Players should not be able to fully block cars unless the game explicitly supports that as a special temporary mechanic.

If a layout blocks all valid paths, the server rejects it.

Narrator gag possibility:

> “The cars admire your bold architectural statement and then leave.”

## 12. Economy

WTF needs both personal and faction economies.

### Possible Resources

#### Cash

General currency earned by cleaning cars.

#### Soap

Used for cleaning boosts and tower upgrades.

#### Towels

Used for repairs, emergency defense, and finishing bonuses.

#### Glamour

Cheescakes-flavored combo/style resource.

#### Motivation

Beefcakes-flavored burst/recovery resource.

#### Data Foam

Spacecakes-flavored mutation/research resource.

#### Grime

Negative global resource that threatens the city.

### Economy Goals

- Every action matters.
- Avoid meaningless inflation.
- Support short-session rewards.
- Give hardcore players strategic spending decisions.
- Prevent one player from draining shared resources.
- Keep faction progress visible.

## 13. Boss Abilities

Each faction boss should have active and passive abilities.

Boss abilities give factions personality and create dramatic rally moments.

### Beefcakes Boss Ability Examples

#### Flex Rush

For a short time, Brush Stations and Spray Hoses gain cleaning power.

#### Protein Foam

Emergency defense boost against heavy vehicles.

#### Leg Day

Slows incoming cars while towers work harder.

### Cheescakes Boss Ability Examples

#### Spotlight Finish

Wax and Dryer stages generate bonus score for perfectly cleaned cars.

#### Glamour Chain

Clean streaks multiply faster for a limited time.

#### Curtain Call

Recover bonus rewards from a nearly failed wave if the final cars are cleaned well.

### Spacecakes Boss Ability Examples

#### Reality Rinse

Temporarily changes how certain towers interact.

#### Quantum Detour

Reroutes a portion of incoming cars.

#### Foam Singularity

Absorbs a messy situation and converts part of it into Data Foam.

## 14. Competitive Structure

### Daily Competition

Daily score can measure:

- Cars cleaned
- Rival waves survived
- Rival waves sent
- Customer happiness
- Grime reduced
- Treasury earned
- Perfect washes

### Weekly / Seasonal Competition

Seasonal score can measure:

- Total faction contribution
- Best defense
- Best offense
- Lowest Grime impact
- Most improved faction
- Best comeback
- Funniest disaster survived

### Winners

Winning should matter, but losing should not make players quit.

Rewards can include:

- Cosmetic trophies
- Boss animations
- Faction banners
- Title unlocks
- Seasonal hall of fame
- Temporary next-season starting bonuses

Avoid rewards that create unstoppable snowballing.

## 15. Collaboration Structure

Collaboration happens at two levels.

### Within a Faction

Players collaborate to:

- Upgrade the shared wash
- Defend against waves
- Vote on plans
- Manage treasury
- Optimize layouts
- Build faction culture

### Across Factions

All factions may need to cooperate when:

- Grime is too high
- Server-wide disasters trigger
- Health Inspector events appear
- A special event threatens everyone
- A low-population faction is collapsing too hard

Cross-faction cooperation should be mechanically useful but socially funny.

Example message:

> “The Health Inspector has arrived. Temporary truce recommended. The Beefcakes refuse to put on shirts.”

## 16. UX / UI

The UI must make a persistent multiplayer system understandable.

### Main Screens

#### Landing / Faction Select

- Shows all three bosses
- Shows current faction standings
- Shows “Join a Shift” call to action
- Explains Big Game in one sentence

#### Faction Dashboard

- Current faction score
- Wash health
- Incoming waves
- Current goals
- Treasury
- Grime Meter
- Recent action log
- Vote/proposal area

#### Wash View

- Visual car-wash layout
- Towers
- Incoming cars
- Cleanliness feedback
- Current wave progress
- Useful action buttons

#### Rival View

- Shows other factions’ status
- Shows attack options
- Shows public rivalry stats
- Avoids revealing hidden information if secrecy is part of the design

#### Proposal / Voting View

- Upgrade votes
- Layout proposal votes
- Transfer notices
- Emergency decisions

### UX Principles

- The next useful action should always be obvious.
- Casual actions should be big and friendly.
- Hardcore details should be available but not mandatory.
- Player contributions should produce visible feedback.
- Faction identity should be visually loud.
- Mobile should be supported from the start, even if the deepest layout tools are desktop-first.

## 17. Art Direction

### Overall Style

- Clean, readable, stylized 2D
- Bright car-wash colors
- Heavy use of foam, shine, bubbles, towels, chrome, and spray
- Comedic character portraits
- Readable cars and towers at small sizes
- Satisfying wash-stage effects

### Character Direction

The factions should be ridiculous but affectionate.

The joke is not:

> “These types of people are bad.”

The joke is:

> “Car-wash branding has escalated into mythological nonsense.”

### Beefcakes Visual Language

- Muscles
- Chrome
- Blue/white foam
- Sporty energy
- Flexing signage
- Strong silhouettes

### Cheescakes Visual Language

- Retro glamour
- Pink/cream/red accents
- Sparkle
- Stage lights
- Shiny finishes
- Elegant signage

### Spacecakes Visual Language

- Alien geometry
- Robot limbs
- Tentacle tools
- Neon soap
- Glitchy foam
- Cosmic signage

## 18. Audio Direction

### Goals

- Light, satisfying sound effects
- Clear feedback for success/failure
- Funny boss voice stingers
- UI sounds that feel bubbly and responsive
- Car sounds that are expressive but not annoying

### Possible Audio Cues

- Scrub
- Rinse
- Wax shine
- Dryer blast
- Cash earned
- Wave incoming
- Boss ability activated
- Grime warning
- Perfect clean
- Faction victory

## 19. Technical Direction

WTF should use an authoritative backend.

### Recommended High-Level Architecture

```text
Browser Client
    ↓ REST / WebSocket
WTF Backend Server
    ↓
Database
    ↓
Persistent Faction State
```

### Client Responsibilities

The browser client should:

- Render the game state
- Capture player input
- Send action requests
- Animate server-approved events
- Display faction dashboards
- Display logs, votes, and results

The client should not be trusted to decide important outcomes.

### Backend Responsibilities

The backend should:

- Manage accounts and sessions
- Manage faction membership
- Store persistent faction state
- Validate tower placement
- Validate spending
- Validate wave sending
- Simulate waves
- Resolve tower effects
- Emit events to connected clients
- Maintain action logs
- Run scheduled events
- Enforce anti-griefing rules
- Store telemetry for balance
- Prevent obvious cheating

### Communication Model

Example action flow:

```text
Player clicks: Place Brush Station at B4
Client sends: place_tower { faction, slot, towerType }
Server checks:
    - player has permission
    - slot exists
    - faction can afford it
    - path remains valid
    - cooldowns allow it
Server responds:
    - approved or denied
    - updated faction state
    - broadcast event
Client animates:
    - tower placement
    - resource change
    - log entry
```

## REST vs WebSocket

Use both if useful:

### REST

Good for:

- Login
- Fetching profiles
- Fetching faction state
- Submitting votes
- Reading history

### WebSocket

Good for:

- Live wave updates
- Tower firing events
- Incoming attacks
- Boss abilities
- Action log updates
- Real-time faction activity

## Deployment Notes

Target deployment model:

- WTF lives at `washtowelfill.io`
- Web app served from its own domain/vhost
- Backend can be hosted as part of the same project or via a shared API origin such as `api.silverwaregames.com`
- The server should be compatible with the Silverware Games DigitalOcean deployment strategy

---

## 20. Data Model Sketch

This is not final schema, but a planning model.

### Player

- id
- displayName
- currentFaction
- accountLevel
- titles
- cosmetics
- trustLevel
- contributionStats
- createdAt
- lastActiveAt

### Faction

- id
- name
- bossName
- treasury
- score
- grimeImpact
- upgradeLevels
- activeBuffs
- seasonalStats
- memberCount
- createdAt

### WashState

- factionId
- layout
- towers
- paths
- activeCars
- incomingWaves
- maintenanceState
- savedPlans
- updatedAt

### Tower

- id
- factionId
- slotId
- type
- level
- state
- cooldown
- placedBy
- upgradedBy

### Wave

- id
- sourceFaction
- targetFaction
- carList
- status
- sentBy
- cost
- reward
- createdAt
- resolvedAt

### ActionLog

- id
- actorPlayerId
- factionId
- actionType
- payload
- visibility
- createdAt

### Proposal

- id
- factionId
- proposedBy
- type
- payload
- votesFor
- votesAgainst
- status
- expiresAt

## 21. MVP Scope

### MVP Goal

Prove the Big Game multiplayer loop with three persistent factions.

The MVP does not need full tower-defense simulation at first.

It needs to prove that players can join a persistent faction, contribute, see shared progress, and create competitive/collaborative server drama.

### Phase 1: Three Persistent Factions

Build:

- Faction select
- Beefcakes / Cheescakes / Spacecakes
- Player membership
- Faction dashboard
- Shared score
- Shared treasury
- Simple contribution actions
- Action log
- Basic daily reset or daily goal

Player actions:

- Claim shift
- Donate towels
- Scrub
- Repair
- Vote on upgrade

Success criteria:

- A player can join a faction.
- Their action changes faction state.
- Other players can see it.
- The server persists it.

### Phase 2: Basic Car-Wash Simulation

Build:

- Simple car path
- Basic towers
- Basic cars
- Cleanliness values
- Rewards for cleaned cars
- Server-side simulation
- Client-side animation of server events

Success criteria:

- The backend can simulate cars moving through a wash.
- Towers affect cars.
- Cleaned cars generate rewards.
- Results are not client-authoritative.

### Phase 3: Rival Waves

Build:

- Send wave action
- Target rival faction
- Incoming wave queue
- Defensive actions
- Wave resolution
- Public attack log

Success criteria:

- One faction can send a dirty wave to another.
- The target faction can defend.
- Results affect both factions.

### Phase 4: Grime Meter

Build:

- Global Grime value
- Grime sources
- Grime penalties
- Shared cleanup events
- City-wide success/failure states

Success criteria:

- Players understand that attacking recklessly can harm everyone.
- Temporary cooperation becomes useful.

### Phase 5: Layout Governance

Build:

- Tower placement proposals
- Voting
- Trusted roles
- Anti-grief validation
- Saved layouts
- Foreman/Architect tools

Success criteria:

- Hardcore players can optimize.
- Casual players can participate through votes.
- Trolls cannot easily destroy the shared wash.

### Phase 6: Seasons, Retention, and Social Layer

Build:

- Weekly/seasonal scoreboards
- Seasonal rewards
- Faction titles
- Boss animations
- Hall of fame
- Event calendar
- Optional faction chat or Discord integration

Success criteria:

- Players have a reason to return.
- Factions develop identity and history.
- The game produces stories.

## 22. Balance Questions

Open questions:

1. How often should faction seasons reset?
2. Should faction membership be locked during the final stretch of a season?
3. How much should population imbalance be corrected automatically?
4. Should underdog factions receive catch-up bonuses?
5. Should the Grime Meter punish everyone equally or mostly the faction causing the mess?
6. How much information should rival factions be able to see?
7. Are layout changes real-time, proposal-based, or limited to planning windows?
8. Should the game support anonymous casual play before login?
9. What is the minimum viable simulation tick rate?
10. Should boss abilities be manually activated, vote-activated, or automatically triggered?

## 23. Tone Rules

WTF should be funny, not cruel.

### Do

- Be ridiculous.
- Be playful.
- Make all factions equally silly.
- Let players love their faction.
- Use innuendo carefully and cartoonishly.
- Make the third faction cosmic and strange rather than “mocking identity.”
- Punch up at branding, corporate competition, and absurd game mechanics.

### Do Not

- Make the joke “men are dumb / women are vain / nonbinary people are weird.”
- Make one faction the “normal” faction and another the “freak” faction.
- Let sexiness become the only identity of the Beefcakes or Cheescakes.
- Let multiplayer competition become harassment.
- Let hardcore players make casual players irrelevant.

## 24. Issue Tracker

Use the GitHub issue tracker for bugs, design discussion, and implementation tasks.

Suggested issue labels:

- `type: bug`
- `type: design`
- `type: feature`
- `type: balance`
- `type: backend`
- `type: frontend`
- `type: art`
- `type: audio`
- `type: writing`
- `priority: p0`
- `priority: p1`
- `priority: p2`
- `priority: p3`
- `status: triage`
- `status: ready`
- `status: in-progress`
- `status: blocked`

Suggested issue title prefixes:

- `[DESIGN]`
- `[BACKEND]`
- `[CLIENT]`
- `[BALANCE]`
- `[ART]`
- `[AUDIO]`
- `[COPY]`

## Community Submission Rules

- Submissions should relate to Wash Towel Fill.
- Bugs, design ideas, balancing notes, and usability feedback are welcome.
- Silverware Games decides whether and when to accept suggestions.
- Public issue submissions do not imply payment, ownership transfer, or guaranteed inclusion.
- Security vulnerabilities should be reported privately, not through public issues.
- Be respectful and follow GitHub Community Guidelines.

## 25. Current Replacement Summary

This document replaces the older “each player owns a car wash” structure with the new Big Game model.

### Preserved From the Older GDD

- Browser-based strategy game
- Tower defense / tower-wars structure
- Multiplayer
- Car wash theme
- Placing and upgrading towers
- Cars pathfinding through wash stages
- Sending waves of cars
- Team-based goals
- Backend-driven multiplayer
- Asynchronous play
- Short-session-friendly goals
- Towers such as Brush, Spray Hose, Wax Applicator, and Dryer Station
- Car types such as Old Rusty Car, Muddy Truck, Luxury Sedan, and Fleet Vehicles

## Changed In This Revision

- Players no longer primarily own private car washes.
- The server owns three permanent faction car washes.
- Players choose a boss/faction and contribute to shared persistent state.
- The three factions compete and collaborate.
- The city-wide Grime Meter creates shared stakes.
- Anti-griefing and role governance become central.
- The game is framed as a Big Game.

## Final Design North Star

> **Three washes. One city. Everyone gets wet. Nobody gets drowned.**

WTF should feel like a living multiplayer comedy machine: part tower defense, part faction war, part shared server toy, part absurd car-wash soap opera.

A player should be able to log in for thirty seconds and help.

A hardcore strategist should be able to spend a whole night optimizing the wash.

A faction should be able to develop its own culture.

And every season should leave behind stories players want to retell:

> “Remember when the Spacecakes accidentally turned all the dryers into portals?”  
> “Remember when the Cheescakes saved the city during the Pollen Apocalypse?”  
> “Remember when the Beefcakes flexed so hard the Health Inspector quit?”


Discord: https://discord.silverwaregames.com (#war-tainted-falls-io)
