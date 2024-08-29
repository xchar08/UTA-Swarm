# UTA Swarm

## Overview

In UTA Swarm, teams use strategic units with unique abilities and implement custom Python APIs for coding challenges. Manage resources, deploy units, and engage in tactical battles.

## Resource Generation

- **Generator:** Generates 10 cash per second for deploying and upgrading units.

## How to Win

- **Unit Core:** Each team has a device called the unit core with 500 hp. If it is destroyed, the opposing team wins.

## Unit Actions

Each unit has one action per turn, which can be:
- **Motion:** Move to a different tile.
- **Upgrading:** Enhance the unit or the generator.
- **Ability:** Use a special ability unique to the unit.
- **Basic Attack:** Perform a standard attack.

## Units

### Basic Units

1. **Warrior**
   - **Price:** 50 cash
   - **Attack:** 10
   - **Health:** 100
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 0
   - **Description:** A simple melee unit with standard attack capabilities.

2. **Brute** (Upgraded Warrior)
   - **Price:** 100 cash
   - **Upgrade Price:** 75 cash
   - **Attack:** 15
   - **Health:** 120
   - **Defense:** 10
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Rage* - Boosts the strength and speed of adjacent allies for 2 seconds, turning them purple with a graphic effect.

3. **Cyborg**
   - **Price:** 80 cash
   - **Attack:** 12 (Laser Beam)
   - **Health:** 90
   - **Defense:** 8
   - **Ranged Attack:** 15
   - **Ranged Defense:** 10
   - **Description:** Shoots laser beams in a line with 2 range, capable of ground-air attacks.

4. **Mainframe** (Upgraded Cyborg)
   - **Price:** 150 cash
   - **Upgrade Price:** 100 cash
   - **Attack:** 20 (Pulsing Attack)
   - **Health:** 110
   - **Defense:** 12
   - **Ranged Attack:** 25
   - **Ranged Defense:** 15
   - **Special Ability:** *Pulsing Attack* - Deals extra damage in an AoE after a 2-turn charge.

5. **Assassin**
   - **Price:** 60 cash
   - **Attack:** 8
   - **Health:** 70
   - **Defense:** 3
   - **Ranged Attack:** 0
   - **Ranged Defense:** 2
   - **Special Ability:** *Enhanced Mobility* - Can move 2 tiles per turn but deals less damage than the Warrior.

6. **Rogue** (Upgraded Assassin)
   - **Price:** 120 cash
   - **Upgrade Price:** 85 cash
   - **Attack:** 12
   - **Health:** 80
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Invisibility* - Becomes untargetable for 1 turn.

7. **Aerial**
   - **Price:** 70 cash
   - **Attack:** 10
   - **Health:** 60
   - **Defense:** 2
   - **Ranged Attack:** 10
   - **Ranged Defense:** 8
   - **Special Ability:** *Flight* - Can fly above obstacles, making it weaker but less vulnerable.

8. **Dragon** (Upgraded Aerial)
   - **Price:** 200 cash
   - **Upgrade Price:** 150 cash
   - **Attack:** 20
   - **Health:** 100
   - **Defense:** 10
   - **Ranged Attack:** 20
   - **Ranged Defense:** 12
   - **Special Abilities:** Air-air and air-ground attack capabilities.

9. **Archer**
   - **Price:** 90 cash
   - **Attack:** 12
   - **Health:** 80
   - **Defense:** 4
   - **Ranged Attack:** 20
   - **Ranged Defense:** 8
   - **Special Ability:** *Piercing Arrow* - Can attack both ground and air units.

10. **Balloon** (Upgraded Archer)
    - **Price:** 140 cash
    - **Upgrade Price:** 100 cash
    - **Attack:** 15
    - **Health:** 90
    - **Defense:** 5
    - **Ranged Attack:** 22
    - **Ranged Defense:** 10
    - **Special Ability:** *Bomb Drop* - Performs an air-ground AoE attack.

11. **Bomber Balloon** (Upgraded Balloon)
    - **Price:** 180 cash
    - **Upgrade Price:** 130 cash
    - **Attack:** 18
    - **Health:** 100
    - **Defense:** 6
    - **Ranged Attack:** 25
    - **Ranged Defense:** 12
    - **Special Ability:** *Enhanced Bomb Drop* - Increased AoE damage.

12. **Thief**
    - **Price:** 70 cash
    - **Attack:** 6
    - **Health:** 60
    - **Defense:** 2
    - **Ranged Attack:** 0
    - **Ranged Defense:** 2
    - **Special Ability:** *Steal* - Can steal an enemy's ability if within 2 tiles.

13. **Dreadknight** (Upgraded Thief)
    - **Price:** 130 cash
    - **Upgrade Price:** 90 cash
    - **Attack:** 10
    - **Health:** 70
    - **Defense:** 4
    - **Ranged Attack:** 0
    - **Ranged Defense:** 4
    - **Special Ability:** *Parry* - Disables an enemy's ability to attack for 1 turn.

14. **Pyrotechnic**
    - **Price:** 200 cash
    - **Attack:** 15
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 20
    - **Ranged Defense:** 8
    - **Special Ability:** *Inferno Blast* - High damage AoE attack with a burning effect over 3 seconds. 
   
15. **Astronaut** (Upgraded Pyrotechnic)
    - **Price:** 600 cash
    - **Attack:** 20
    - **Health:** 80
    - **Defense:** 5
    - **Ranged Attack:** 25
    - **Ranged Defense:** 6
    - **Special Ability:** *Meteor Shower* - Massive AoE damage from above. Multiple 'inferno blasts' with Persisting status field. Can only use ability every 20 turns.

16. **Hippee**
    - **Price:** 500 cash
    - **Attack:** 12
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 15
    - **Ranged Defense:** 8
    - **Special Ability:** *Grow* - Roots all enemies for 3 turns.
   
17. **Guardian of Nature** (Upgraded Hippee)
    - **Price:** 140 cash
    - **Attack:** 10
    - **Health:** 120
    - **Defense:** 15
    - **Ranged Attack:** 0
    - **Ranged Defense:** 10
    - **Special Ability:** *Plant Wall* - Reduces damage taken by adjacent allies.

18. **Golem**
    - **Price:** 180 cash
    - **Attack:** 20
    - **Health:** 150
    - **Defense:** 20
    - **Ranged Attack:** 0
    - **Ranged Defense:** 15
    - **Special Ability:** *Earthquake* - Causes tremors that damage and disrupt enemy formations.

19. **Healer**
    - **Price:** 110 cash
    - **Attack:** 8
    - **Health:** 70
    - **Defense:** 5
    - **Ranged Attack:** 15
    - **Ranged Defense:** 8
    - **Special Ability:** *Midas Touch* - Heals allied units and removes debuffs.

20. **Behemoth**
    - **Price:** 200 cash
    - **Attack:** 25
    - **Health:** 180
    - **Defense:** 25
    - **Ranged Attack:** 0
    - **Ranged Defense:** 20
    - **Special Ability:** *Titan Smash* - Heavy damage and knockback in AoE.

21. **Banshee** (Upgraded Behemoth)
    - **Price:** 90 cash
    - **Attack:** 14
    - **Health:** 60
    - **Defense:** 3
    - **Ranged Attack:** 18
    - **Ranged Defense:** 7
    - **Special Ability:** *Wail of Despair* - Reduces enemy attack power and speed.

## Training Playground

Teams can create a custom training playground for their AI, allowing simulation and testing of strategies and unit interactions.
