# Wash Towel Fill – Game Design Document (GDD)
![Cover Image of Cheescake and Beefcake](https://i.imgur.com/gTym87U.png)

## High Concept
**Wash Towel Fill** is a browser-based, multiplayer **tower-wars / tower-defense hybrid** inspired by games like *Clash of Clans*.  
Each player owns and upgrades a **Car Wash**, placing wash equipment and employees (towers) along a path to process incoming cars through multiple cleaning stages.

Players **send waves of cars** to other players’ car washes to strengthen their own team and push shared goals, creating a mix of **offense, defense, and team-based progression**.

Also there is plenty of beefcake and cheescake to go around!

## Genre
- Strategy
- Tower Defense
- Asynchronous Multiplayer
- Social / Team-Based

## Platforms
- Web browser (desktop & mobile)
- Backend-driven multiplayer (accounts, teams, stats)

## Core Gameplay Loop
1. Player logs in and manages their Car Wash.
2. Player places, upgrades, or rearranges towers.
3. Player sends waves of cars to other players.
4. Incoming cars pathfind through the wash stages.
5. Performance generates resources and team progress.
6. Resources are reinvested into upgrades and strategy.
7. Loop repeats with increasing difficulty and stakes.

## Player Car Wash
Each player owns a **customizable Car Wash layout**.

### Key Elements
- Cars can path find to find shortest path to end of the car wash.
- Build slots stack, combining synergies between towers.
- Towers interact with cars as they pass through stages
- Layout decisions directly affect performance

## Towers (Wash Stages)
Towers represent **wash equipment or staff**, each focused on a specific stage of cleaning.

### Example Tower Types
- **Brush Station**
  - Removes heavy dirt
  - Slow but strong
- **Spray Hose**
  - Medium dirt removal
  - Faster throughput
- **Wax Applicator**
  - Adds score multipliers
  - Synergy-focused
- **Dryer Station**
  - Finalizes cleaning
  - Converts cleanliness into score

### Tower Properties
- Cost
- Effect type (cleaning, buff, debuff)
- Throughput / cooldown
- Upgrade tiers
- Synergies with other towers

## Cars (Enemy Units)
Cars act as the “units” in tower-defense gameplay.

### Example Car Types
- Old Rusty Car – high dirt, slow
- Muddy Truck – resistant to early cleaning
- Luxury Sedan – low dirt, high score potential
- Fleet Vehicles – appear in waves

### Car Properties
- Dirt level
- Speed
- Special traits or resistances
- Score value when fully cleaned

## Sending Waves (Offense)
Players can send **waves of cars** to other players’ car washes.

- Waves scale in difficulty and reward
- Sending cars benefits the sender’s **team**
- Defensive layouts must adapt to real player behavior
- Encourages scouting and meta strategies

## Multiplayer & Teams
### Teams
- Players join or form teams
- Teams contribute toward shared goals
- Team performance unlocks bonuses

### Team Goals
- Weekly or seasonal objectives
- Global or team-only leaderboards
- Cooperative progress with competitive pressure

## Progression
### Player Progression
- Levels unlock new towers or upgrades
- Visual customization options
- Increased layout flexibility

### Team Progression
- Shared bonuses
- Seasonal milestones
- Prestige or reset mechanics (TBD)

## Economy
- Resources earned by cleaning cars successfully
- Sending cars is an investment with risk/reward
- Economy designed so **every action matters**
- No meaningless currency inflation

## UX / UI
- Drag-and-drop tower placement
- Clear path visualization
- Fast feedback on car cleanliness
- Team dashboard showing shared progress
- Mobile-friendly interactions

## Art Direction
- Clean, readable, stylized 2D
- Satisfying visual feedback for wash stages
- Readable towers and cars at a glance

## Audio
- Light, satisfying sound effects
- Clear feedback for success/failure
- Minimal but expressive UI sounds

## Technical Notes
- Fully browser-based client
- Backend handles:
  - Accounts
  - Teams
  - Progression
  - Wave sending
- Asynchronous multiplayer
- Designed for scalability

## Design Goals
- Easy to understand, hard to master
- Strong team-based motivation
- Meaningful strategic choices
- No filler systems
- Fun even in short sessions

## Known Design Questions
- Path flexibility vs fixed lanes
- Tower slot limits
- Anti-griefing / fair matchmaking
- Optimal session length

(Tracked in GitHub Issues)

## Related Documents
- Issues Tracker:  
  https://github.com/Silverware-Games/wash-towel-fill-gdd/issues

## Status
🚧 **Active Design / Iteration Phase**  
This document is a living design and will evolve alongside implementation.


# Issue Tracker
Use https://github.com/Silverware-Games/wash-towel-fill-gdd/issues to submit an idea or a bug report. You should be signed into GitHub.

Rules:

* You must follow GitHub Community Guidelines.
* The bug reports/ideas should be related to War Tainted Falls only.
* It's up to us to decide whether (and when) accept the idea/bug report or not.
* We cannot pay you for any idea you submit, just offer you a free copy of the game.
* All vulnerabilities should be reported privately.
* You must not use the Issue Tracker if you do not agree to any of the terms.

Discord: https://discord.silverwaregames.com (#war-tainted-falls-io)
