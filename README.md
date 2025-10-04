# text based adventure game
A game where you go on a adventure using text instead of a visual screen

Updated readme file

 Struktur:

 rpg-game/
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ game.py # Programstart (CLI)
├─ rpg/
│ ├─ __init__.py
│ ├─ core/
│ │ ├─ __init__.py
│ │ ├─ game.py # Game-loop & tillstånd
│ │ ├─ world.py # World, Location
│ │ └─ data_loader.py # Laddar JSON-data
│ ├─ entities/
│ │ ├─ __init__.py
│ │ ├─ player.py # Player-klass (HP, gold, inventory)
│ │ ├─ npc.py # NPC-klass (dialog, trade)
│ │ ├─ inventory.py # Inventory-klass
│ │ └─ items.py # Item, Weapon, Consumable
│ ├─ systems/
│ │ ├─ __init__.py
│ │ ├─ combat.py # fight
│ │ ├─ dialogue.py # talk to npc
│ │ ├─ movement.py # walk to destination
│ │ ├─ loot.py # pick up items
│ │ └─ trading.py # trade with npc (prio)
│ └─ utils/
│ ├─ __init__.py
│ ├─ io.py # Rich console-UI
│ ├─ save_load.py # spara/ladda (json)
│ └─ time_utils.py # datetime-hjälp
├─ data/
│ ├─ items.json
│ ├─ npcs.json
│ └─ world.json
└─ tests/
├─ __init__.py
└─ test_combat.py

<img width="565" height="525" alt="flowchart" src="https://github.com/user-attachments/assets/4dcf06d2-692a-4cd9-b3bd-2a884573d27a" />


## ✅ Features (planned)

- **Player** with HP, gold and inventory  
- **Combat system** (fight enemies)  
- **Dialogue system** (talk to NPCs)  
- **Movement** (walk to new locations)  
- **Loot** (pick up items)  
- **Trading** (buy items from NPCs)

- - External library: [Rich]
 
  - 



Dungeon Escape – Flow Narrative

Start
You wake on a cold stone floor in a dark corridor. You have 5 gold in your pocket.
Ahead, the corridor splits: left or right?

Left Path – Armory (loot + trading)
A dusty armory. Two intact weapons lie on a rack — Sword or Bow (pick one).
A traveling merchant stands by the door:

Buy Shield for 5 gold (if you can afford it).

(Optional) Pickpocket the shield (40% success → take shield; on fail → lose 2 HP and the merchant throws you out).

Right Path – Wizard’s Laboratory (loot)
An old lab. You find 1 Health Potion (restores HP).

The Dying Prisoner (talk + moral + companion)
A wounded prisoner whispers: “Give me a potion… I’ll give you the key.”
Choices:

Give potion → you receive the Key and the prisoner becomes a Companion (+10% combat chance).

Refuse → continue without key.

Pickpocket Key (50% success; on fail → lose 3 HP).

The Locked Door (gating)

If you have the Key → open the door → room with Armor and a Battle Axe (loot).

If no key → forced left, where a Skeleton awaits.

Skeleton Encounter (combat)
Outcome depends on gear (companion adds +10% to any chance):

. With Sword → 1/3 chance to win.

. With Bow → 1/2 chance to win.

. With Armor + Axe → guaranteed win.

. With No weapon → instant death.

If you have an Invisibility Cloak (see reward below) → you may skip this fight once.

If you lose: restart.
If you win: choose one reward: Shield / Dagger / Invisibility Cloak.

The Dragon’s Lair (final combat)
“You shall not leave alive!” roars the dragon.

Win only if you have Armor + Axe + Shield.

Invisibility Cloak does not fool the dragon.

Otherwise: you die.

Endings

Victory: you strike the final blow and escape into the moonlight.

Defeat: flames engulf you; your soul joins the fallen.
