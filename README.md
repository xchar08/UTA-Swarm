# UTA Swarm

## Overview

UTA Swarm is a strategic game where teams deploy units with unique abilities and implement a custom Python Library to tackle coding challenges. Manage resources, deploy units, and engage in tactical battles to outmaneuver your opponents.

## Resource Generation

- **Generator:** Produces 50 cash per turn to support unit deployment and upgrades.

## Victory Conditions

- **Unit Core:** Each team has a Unit Core with 500 HP. Destroying the opponent's Unit Core secures victory.

## Unit Actions

Each unit can perform one action per turn, which may include:
- **Motion:** Move to a different tile.
- **Upgrade:** Enhance the unit or generator.
- **Ability:** Use the unit's unique special ability.
- **Basic Attack:** Execute a standard attack.

## Unit Prices and Abilities

### Ground Units

1. **Warrior**
   - **Price:** 50 cash
   - **Attack:** 10 (Ground->Ground)
   - **Health:** 100
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 0
   - **Kill Reward:** 25 cash

2. **Brute** (Upgraded Warrior)
   - **Price:** 80 cash (additional to Warrior)
   - **Attack:** 15 (Ground->Ground)
   - **Health:** 120
   - **Defense:** 10
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Rage* - Increases the attack power and movement speed of adjacent allies by 25% for 2 seconds, visually indicated by a purple aura.
   - **Kill Reward:** 40 cash

3. **Archer**
   - **Price:** 80 cash
   - **Attack:** 0
   - **Health:** 80
   - **Defense:** 0
   - **Ranged Attack:** 12 (Ground->Ground Ground->Air)
   - **Ranged Defense:** 0
   - **Special Ability:** *Piercing Arrow* - Can hit both ground and air units, dealing 15 damage with a chance to pierce through 2 targets in a line.
   - **Kill Reward:** 40 cash

4. **Balloon** (Upgraded Archer)
    - **Price:** 120 cash (additional to Archer)
    - **Attack:** 0 
    - **Health:** 90
    - **Defense:** 5
    - **Ranged Attack:** 15 (Air->Ground + Air->Air)
    - **Ranged Defense:** 0
    - **Special Ability:** *Bomb Drop* - Executes an attack dealing 25 damage to all ground units within a 2-tile radius. (Air->Ground, AOE)
    - **Kill Reward:** 60 cash

5. **Bomber Balloon** (Upgraded Balloon)
    - **Price:** 160 cash (additional to Balloon) 
    - **Attack:** 0
    - **Health:** 100
    - **Defense:** 6
    - **Ranged Attack:** 25 (Air->Ground, AOE) or 15 (Air->Ground + Air->Air)
    - **Ranged Defense:** 12
    - **Special Ability:** *Enhanced Bomb Drop* - Increases AoE damage to 35 within a 2-tile radius.
    - **Kill Reward:** 80 cash

6. **Cyborg**
   - **Price:** 70 cash
   - **Attack:** 10
   - **Health:** 90
   - **Defense:** 8
   - **Ranged Attack:** 15 (Ground->Ground, Air->Air)
   - **Ranged Defense:** 10
   - **Kill Reward:** 35 cash

7. **Mainframe** (Upgraded Cyborg)
   - **Price:** 120 cash (additional to Cyborg)
   - **Attack:** 20 (Pulsing Attack)
   - **Health:** 110
   - **Defense:** 12
   - **Ranged Attack:** 25
   - **Ranged Defense:** 15
   - **Special Ability:** *Pulsing Attack* - After a 2-turn charge, emits an AoE pulse dealing 30 damage to all enemies within 3 tiles.
   - **Kill Reward:** 60 cash

8. **Assassin**
   - **Price:** 60 cash
   - **Attack:** 8
   - **Health:** 70
   - **Defense:** 3
   - **Ranged Attack:** 0
   - **Ranged Defense:** 2
   - **Special Ability:** *Enhanced Mobility* - Can move up to 2 tiles per turn and deals 20% less damage than the Warrior but has increased evasion.
   - **Kill Reward:** 30 cash

9. **Rogue** (Upgraded Assassin)
   - **Price:** 100 cash (additional to Assassin)
   - **Attack:** 12
   - **Health:** 80
   - **Defense:** 5
   - **Ranged Attack:** 0
   - **Ranged Defense:** 5
   - **Special Ability:** *Invisibility* - Becomes untargetable for 1 turn, making it immune to all attacks during this period.
   - **Kill Reward:** 50 cash

10. **Golem**
   - **Price:** 220 cash
   - **Attack:** 20
   - **Health:** 150
   - **Defense:** 15
   - **Ranged Attack:** 5
   - **Ranged Defense:** 5
   - **Special Ability:** *Earthquake* - Causes a tremor that damages all units within a 2-tile radius for 25 damage and reduces their movement speed by 50% for 2 turns.
   - **Kill Reward:** 110 cash

11. **Meteor Golem** (Upgraded Golem)
   - **Price:** 250 cash (additional to Golem)
   - **Attack:** 25
   - **Health:** 200
   - **Defense:** 20
   - **Ranged Attack:** 10
   - **Ranged Defense:** 10
   - **Special Ability:** *Meteor Shower* - Launches a meteor strike that deals 40 damage to all units within a 3-tile radius and causes burning effects dealing 15 additional damage over 4 seconds.
   - **Kill Reward:** 125 cash

12. **Golem King** (Upgraded Golem)
   - **Price:** 320 cash (additional to Golem)
   - **Attack:** 30
   - **Health:** 200
   - **Defense:** 20
   - **Ranged Attack:** 0
   - **Ranged Defense:** 15
   - **Special Ability:** *Grand Quake* - Deals 40 damage in a massive 4-tile radius, reducing the movement speed of all units within range by 75% for 3 turns.
   - **Kill Reward:** 160 cash

13. **Thief**
    - **Price:** 70 cash
    - **Attack:** 6
    - **Health:** 60
    - **Defense:** 2
    - **Ranged Attack:** 0
    - **Ranged Defense:** 2
    - **Special Ability:** *Steal* - Can steal an enemy’s ability within 2 tiles, copying their special ability for 1 turn.
    - **Kill Reward:** 35 cash

14. **Hippee**
    - **Price:** 300 cash
    - **Attack:** 12
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 15
    - **Ranged Defense:** 8
    - **Special Ability:** *Grow* - Roots all enemies within a 2-tile radius for 3 turns, preventing their movement and reducing their attack power by 30%.
    - **Kill Reward:** 150 cash

15. **Guardian of Nature** (Upgraded Hippee)
    - **Price:** 160 cash (additional to Hippee)
    - **Attack:** 10
    - **Health:** 120
    - **Defense:** 15
    - **Ranged Attack:** 0
    - **Ranged Defense:** 10
    - **Special Ability:** *Plant Wall* - Creates a defensive barrier reducing damage taken by adjacent allies by 50% for 2 turns.
    - **Kill Reward:** 80 cash

16. **Ninja**
    - **Price:** 70 cash
    - **Attack:** 8
    - **Health:** 60
    - **Defense:** 4
    - **Ranged Attack:** 0
    - **Ranged Defense:** 5
    - **Special Ability:** *Shadow Strike* - Can attack an enemy from the shadows, dealing double damage if the enemy is not adjacent.
    - **Kill Reward:** 35 cash

17. **Master Ninja** (Upgraded Ninja)
    - **Price:** 120 cash (additional to Ninja)
    - **Attack:** 14
    - **Health:** 80
    - **Defense:** 8
    - **Ranged Attack:** 0
    - **Ranged Defense:** 8
    - **Special Ability:** *Ultimate Shadow Strike* - Deals triple damage to any enemy not adjacent and applies a stun effect for 1 turn.
    - **Kill Reward:** 60 cash

18. **Behemoth**
    - **Price:** 250 cash
    - **Attack:** 25
    - **Health:** 180
    - **Defense:** 25
    - **Ranged Attack:** 0
    - **Ranged Defense:** 20
    - **Special Ability:** *Titan Smash* - Deals 50 damage and causes knockback within a 2-tile radius, displacing affected units by 1 tile.
    - **Kill Reward:** 125 cash

19. **Banshee** (Upgraded Behemoth)
    - **Price:** 90 cash 
    - **Attack:** 14
    - **Health:** 50
    - **Defense:** 2
    - **Ranged Attack:** 0
    - **Ranged Defense:** 4
    - **Special Ability:** *Wail* - Causes fear in all enemy units within a 2-tile radius, reducing their attack and defense by 20% for 2 turns.
    - **Kill Reward:** 45 cash

20. **Wraith** (Upgraded Banshee)
    - **Price:** 140 cash (additional to Banshee)
    - **Attack:** 20
    - **Health:** 60
    - **Defense:** 5
    - **Ranged Attack:** 0
    - **Ranged Defense:** 6
    - **Special Ability:** *Phantom Strike* - Deals 30 damage to an enemy within a 2-tile radius and reduces their movement speed by 50% for 2 turns.
    - **Kill Reward:** 70 cash

21. **Titan**
    - **Price:** 250 cash
    - **Attack:** 30
    - **Health:** 180
    - **Defense:** 20
    - **Ranged Attack:** 0
    - **Ranged Defense:** 12
    - **Special Ability:** *Ground Smash* - Deals 60 damage in a 4-tile radius, knocking back enemies and stunning them for 2 turns.
    - **Kill Reward:** 125 cash

22. **Pyrotechnic**
    - **Price:** 180 cash
    - **Attack:** 15
    - **Health:** 80
    - **Defense:** 6
    - **Ranged Attack:** 20
    - **Ranged Defense:** 8
    - **Special Ability:** *Inferno Blast* - Deals 40 damage in an AoE to all units within a 3-tile radius, with a burning effect causing an additional 10 damage over 3 seconds.
    - **Kill Reward:** 90 cash

23. **Fire Lord** (Upgraded Pyrotechnic)
    - **Price:** 320 cash (additional to Pyrokinetic)
    - **Attack:** 30
    - **Health:** 80
    - **Defense:** 10
    - **Ranged Attack:** 35
    - **Ranged Defense:** 8
    - **Special Ability:** Inferno Wave - Deals 40 damage to all enemies within a 3-tile radius and causes them to burn for an additional 20 damage over 5 seconds. Usable every 10 turns.
    - **Kill Reward:** 160 cash

24. **Astronaut** (Upgraded Pyrotechnic)
    - **Price:** 400 cash (additional to Pyrotechnic)
    - **Attack:** 20
    - **Health:** 80
    - **Defense:** 5
    - **Ranged Attack:** 25
    - **Ranged Defense:** 6
    - **Special Ability:** *Meteor Shower* - Deals 50 damage in a massive AoE with a 5-tile radius, inflicting continuous inferno effects that deal 15 additional damage over 5 seconds. Usable every 20 turns.
    - **Kill Reward:** 200 cash

25. **Teslas** (Upgraded Pyrotechnic)
   - **Price:** To be determined, but cheaper than Astronaut
   - **Attack:** Chains attacks with a range of 3 tiles, and can chain further if enemy units are adjacent
   - **Health:** Lower than Pyrotechnic
   - **Special Ability:** *Disruptor Pulse* - Has a small chance to disable a unit's attack for 2 turns
   - **Description:** Has low health and can attack in a chain, with an additional effect if enemies are next to each other. Serves as an alternate upgrade to the Pyrotechnic.
   - **Kill Reward:** To be determined

26. **Electromancer** (Upgraded Tesla)
    - **Price:** 120 cash (additional to Tesla)
    - **Attack:** 18
    - **Health:** 80
    - **Defense:** 8
    - **Ranged Attack:** 20
    - **Ranged Defense:** 8
    - **Special Ability:** *Electrify* - Increases chain attack damage to 30 per target and has a 20% chance to disable an enemy unit’s attack for 2 turns.
    - **Kill Reward:** 60 cash

27. **Thunder Titan** (Upgraded Tesla)
    - **Price:** 150 cash (additional to Tesla)
    - **Attack:** 18 (Chain Lightning)
    - **Health:** 80
    - **Defense:** 8
    - **Ranged Attack:** 20
    - **Ranged Defense:** 10
    - **Special Ability:** Electromagnetic Burst - Chain Lightning effect with increased damage, dealing 15 damage to the first enemy and 10 damage to subsequent enemies, with a small chance to disable a unit’s attack for 2 turns.
    - **Kill Reward:** 75 cash

28. **Healer**
    - **Price:** 100 cash
    - **Attack:** 0
    - **Health:** 70
    - **Defense:** 4
    - **Ranged Attack:** 0
    - **Ranged Defense:** 5
    - **Special Ability:** *Healing Aura* - Restores 20 HP to all adjacent units each turn.
    - **Kill Reward:** 50 cash

29. **Kakit** (Upgraded Healer)
    - **Price:** 150 cash (additional to Healer)
    - **Attack:** 0
    - **Health:** 90
    - **Defense:** 6
    - **Ranged Attack:** 0
    - **Ranged Defense:** 8
    - **Special Ability:** *Blessing* - Provides a 25% damage boost and 20 HP healing to all adjacent allies for 2 turns.
    - **Kill Reward:** 75 cash

30. **Penye** (Upgraded Healer)
    - **Price:** 160 cash (additional to Healer)
    - **Upgrade Price:** 100 cash
    - **Attack:** 10
    - **Health:** 90
    - **Defense:** 10
    - **Ranged Attack:** 0
    - **Ranged Defense:** 10
    - **Special Ability:** *Divine Aura* - Heals all allied units within a 3-tile radius by 50 health points and provides a shield that absorbs 20 damage for 2 turns.
    - **Kill Reward:** 80 cash

31. **Aerial**
   - **Price:** 80 cash
   - **Attack:** 10
   - **Health:** 60
   - **Defense:** 2
   - **Ranged Attack:** 20 (Projectile)
   - **Ranged Defense:** 4
   - **Special Ability:** *Sonic Boom* - Deals 25 damage to all units within a 2-tile radius and causes disorientation, reducing their accuracy by 50% for 2 turns.
   - **Kill Reward:** 40 cash

32. **Interceptor** (Upgraded Aerial)
   - **Price:** 120 cash (additional to Aerial)
   - **Attack:** 20
   - **Health:** 80
   - **Defense:** 5
   - **Ranged Attack:** 30 (Guided Missile)
   - **Ranged Defense:** 10
   - **Special Ability:** *Missile Barrage* - Launches 3 guided missiles, each dealing 20 damage and applying a 1-turn burn effect to enemies.
   - **Kill Reward:** 60 cash

33. **Phoenix** (Upgraded Interceptor)
   - **Price:** 180 cash (additional to Intrceptor)
   - **Attack:** 15
   - **Health:** 100
   - **Defense:** 8
   - **Ranged Attack:** 25 (Fireballs)
   - **Ranged Defense:** 12
   - **Special Ability:** *Firestorm* - Summons a storm of fireballs that deal 30 damage in a 3-tile radius, igniting enemies for 10 additional damage over 2 turns.
   - **Kill Reward:** 90 cash

34. **Stormbringer** (Upgraded Phoenix)
   - **Price:** 200 cash (additional to Phoenix)
   - **Attack:** 30
   - **Health:** 120
   - **Defense:** 10
   - **Ranged Attack:** 35 (Thunder Strike)
   - **Ranged Defense:** 15
   - **Special Ability:** *Thunderstorm* - Calls down a powerful lightning storm dealing 50 damage and stunning enemies within a 4-tile radius for 2 turns.
   - **Kill Reward:** 100 cash

35. **Dragon** (Upgraded Interceptor)
   - **Price:** 400 cash (additional to Intrceptor)
   - **Attack:** 40
   - **Health:** 150
   - **Defense:** 20
   - **Ranged Attack:** 40 (Fire Breath)
   - **Ranged Defense:** 20
   - **Special Ability:** *Inferno Breath* - Unleashes a fiery breath attack that deals 60 damage in a 5-tile line, causing burning for 20 damage over 4 turns.
   - **Kill Reward:** 150 cash

