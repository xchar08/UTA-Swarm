# UTA Swarm

## Overview

UTA Swarm is a strategic game where teams deploy units with unique abilities and implement custom Python APIs to tackle coding challenges. Manage resources, deploy units, and engage in tactical battles to outmaneuver your opponents.

## Resource Generation

- **Generator:** Produces 10 cash per second to support unit deployment and upgrades.

## Victory Conditions

- **Unit Core:** Each team has a Unit Core with 500 HP. Destroying the opponent's Unit Core secures victory.

## Unit Actions

Each unit can perform one action per turn, which may include:
- **Motion:** Move to a different tile.
- **Upgrade:** Enhance the unit or generator.
- **Ability:** Use the unit's unique special ability.
- **Basic Attack:** Execute a standard attack.

## Unit Prices and Abilities

### Basic Units

1. **Warrior**
   - **Price:** 50 cash
   - **Attack:** 10
   - **Health:** 100
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 0
   - **Description:** A reliable melee unit with balanced stats.
   - **Kill Reward:** 25 cash

2. **Brute** (Upgraded Warrior)
   - **Price:** 80 cash (additional to Warrior)
   - **Upgrade Price:** 50 cash
   - **Attack:** 15
   - **Health:** 120
   - **Defense:** 10
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Rage* - Increases the attack power and movement speed of adjacent allies by 25% for 2 seconds, visually indicated by a purple aura.
   - **Kill Reward:** 40 cash

3. **Cyborg**
   - **Price:** 70 cash
   - **Attack:** 12 (Laser Beam)
   - **Health:** 90
   - **Defense:** 8
   - **Ranged Attack:** 15
   - **Ranged Defense:** 10
   - **Description:** Fires a continuous laser beam in a line, dealing 12 damage per second to all units in its path (2 range), effective against both ground and air targets.
   - **Kill Reward:** 35 cash

4. **Mainframe** (Upgraded Cyborg)
   - **Price:** 120 cash (additional to Cyborg)
   - **Upgrade Price:** 80 cash
   - **Attack:** 20 (Pulsing Attack)
   - **Health:** 110
   - **Defense:** 12
   - **Ranged Attack:** 25
   - **Ranged Defense:** 15
   - **Special Ability:** *Pulsing Attack* - After a 2-turn charge, emits an AoE pulse dealing 30 damage to all enemies within 3 tiles.
   - **Kill Reward:** 60 cash

5. **Assassin**
   - **Price:** 60 cash
   - **Attack:** 8
   - **Health:** 70
   - **Defense:** 3
   - **Ranged Attack:** 0
   - **Ranged Defense:** 2
   - **Special Ability:** *Enhanced Mobility* - Can move up to 2 tiles per turn and deals 20% less damage than the Warrior but has increased evasion.
   - **Kill Reward:** 30 cash

6. **Rogue** (Upgraded Assassin)
   - **Price:** 100 cash (additional to Assassin)
   - **Upgrade Price:** 60 cash
   - **Attack:** 12
   - **Health:** 80
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Invisibility* - Becomes untargetable for 1 turn, making it immune to all attacks during this period.
   - **Kill Reward:** 50 cash

7. **Aerial**
   - **Price:** 80 cash
   - **Attack:** 10
   - **Health:** 60
   - **Defense:** 2
   - **Ranged Attack:** 10
   - **Ranged Defense:** 8
   - **Special Ability:** *Flight* - Can fly over obstacles and has 50% reduced damage from ground attacks.
   - **Kill Reward:** 40 cash

8. **Dragon** (Upgraded Aerial)
   - **Price:** 160 cash (additional to Aerial)
   - **Upgrade Price:** 100 cash
   - **Attack:** 20
   - **Health:** 100
   - **Defense:** 10
   - **Ranged Attack:** 20
   - **Ranged Defense:** 12
   - **Special Abilities:** Capable of launching air-to-air and air-to-ground attacks with 25 damage per attack.
   - **Kill Reward:** 80 cash

9. **Archer**
   - **Price:** 80 cash
   - **Attack:** 12
   - **Health:** 80
   - **Defense:** 4
   - **Ranged Attack:** 20
   - **Ranged Defense:** 8
   - **Special Ability:** *Piercing Arrow* - Can hit both ground and air units, dealing 15 damage with a chance to pierce through 2 targets in a line.
   - **Kill Reward:** 40 cash

10. **Balloon** (Upgraded Archer)
    - **Price:** 120 cash (additional to Archer)
    - **Upgrade Price:** 70 cash
    - **Attack:** 15
    - **Health:** 90
    - **Defense:** 5
    - **Ranged Attack:** 22
    - **Ranged Defense:** 10
    - **Special Ability:** *Bomb Drop* - Executes an AoE attack dealing 25 damage to all ground units within a 2-tile radius.
    - **Kill Reward:** 60 cash

11. **Bomber Balloon** (Upgraded Balloon)
    - **Price:** 160 cash (additional to Balloon)
    - **Upgrade Price:** 90 cash
    - **Attack:** 18
    - **Health:** 100
    - **Defense:** 6
    - **Ranged Attack:** 25
    - **Ranged Defense:** 12
    - **Special Ability:** *Enhanced Bomb Drop* - Increases AoE damage to 35 within a 2-tile radius.
    - **Kill Reward:** 80 cash

12. **Thief**
    - **Price:** 70 cash
    - **Attack:** 6
    - **Health:** 60
    - **Defense:** 2
    - **Ranged Attack:** 0
    - **Ranged Defense:** 2
    - **Special Ability:** *Steal* - Can steal an enemy’s ability within 2 tiles, copying their special ability for 1 turn.
    - **Kill Reward:** 35 cash

13. **Pyrotechnic**
    - **Price:** 180 cash
    - **Attack:** 15
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 20
    - **Ranged Defense:** 8
    - **Special Ability:** *Inferno Blast* - Deals 40 damage in an AoE to all units within a 3-tile radius, with a burning effect causing an additional 10 damage over 3 seconds.
    - **Kill Reward:** 90 cash

14. **Astronaut** (Upgraded Pyrotechnic)
    - **Price:** 400 cash (additional to Pyrotechnic)
    - **Upgrade Price:** 200 cash
    - **Attack:** 20
    - **Health:** 80
    - **Defense:** 5
    - **Ranged Attack:** 25
    - **Ranged Defense:** 6
    - **Special Ability:** *Meteor Shower* - Deals 50 damage in a massive AoE with a 5-tile radius, inflicting continuous inferno effects that deal 15 additional damage over 5 seconds. Usable every 20 turns.
    - **Kill Reward:** 200 cash

15. **Hippee**
    - **Price:** 300 cash
    - **Attack:** 12
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 15
    - **Ranged Defense:** 8
    - **Special Ability:** *Grow* - Roots all enemies within a 2-tile radius for 3 turns, preventing their movement and reducing their attack power by 30%.
    - **Kill Reward:** 150 cash

16. **Guardian of Nature** (Upgraded Hippee)
    - **Price:** 160 cash (additional to Hippee)
    - **Upgrade Price:** 100 cash
    - **Attack:** 10
    - **Health:** 120
    - **Defense:** 15
    - **Ranged Attack:** 0
    - **Ranged Defense:** 10
    - **Special Ability:** *Plant Wall* - Creates a defensive barrier reducing damage taken by adjacent allies by 50% for 2 turns.
    - **Kill Reward:** 80 cash

17. **Golem**
    - **Price:** 220 cash
    - **Attack:** 20
    - **Health:** 150
    - **Defense:** 20
    - **Ranged Attack:** 0
    - **Ranged Defense:** 15
    - **Special Ability:** *Earthquake* - Causes an earthquake dealing 40 damage to all enemies within a 3-tile radius and reducing their movement speed by 50% for 2 turns.
    - **Kill Reward:** 110 cash

18. **Healer**
    - **Price:** 120 cash
    - **Attack:** 8
    - **Health:** 70
    - **Defense:** 5
    - **Ranged Attack:** 15
    - **Ranged Defense:** 8
    - **Special Ability:** *Midas Touch* - Heals all allied units within a 2-tile radius by 20 HP and removes debuffs.
    - **Kill Reward:** 60 cash

19. **Behemoth**
    - **Price:** 250 cash
    - **Attack:** 25
    - **Health:** 180
    - **Defense:** 25
    - **Ranged Attack:** 0
    - **Ranged Defense:** 20
    - **Special Ability:** *Titan Smash* - Deals 50 damage and causes knockback within a 2-tile radius, displacing affected units by 1 tile.
    - **Kill Reward:** 125 cash

20. **Banshee** (Upgraded Behemoth)
    - **Price:** 120 cash (additional to Behemoth)
    - **Upgrade Price:** 60 cash
    - **Attack:** 14
    - **Health:** 60
    - **Defense:** 3
    - **Ranged Attack:** 18
    - **Ranged Defense:** 7
    - **Special Ability:** *Wail of Despair* - Reduces the attack power and speed of enemies within a 2-tile radius by 30% for 2 turns.
    - **Kill Reward:** 60 cash

## Training Playground

Teams can create a custom training playground to test and refine unit interactions and strategies.
