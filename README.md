# AOTV Pathfinder (Fabric 1.21.11)

Client-side helper for Hypixel SkyBlock AOTV routing.

## Features
- AOTV/AOTE held-item detection
- Live mana parsing from Hypixel action bar
- A* pathfinding with mixed movement:
  - normal AOTV teleport hop (non-shift)
  - etherwarp hop (shift)
  - ground/walking steps when teleport path is blocked
- Teleport planning supports any direction (not facing-locked)
- Gravity-aware teleport chaining for multi up/down teleports
- `/setgoal <x> <y> <z>` command for global goals
- `/preview` to preview AI path to current goal/look block (no movement)
- `/preview <x> <y> <z>` to preview path to explicit coords
- `/preview clear` to clear preview path
- Live AI mode: builds and follows a complete path to the current goal (replans only when needed)
- ESP-style path highlights (thicker non-particle block markers along route)
- Visual feedback in actionbar:
  - landing preview coordinates
  - route preview of next steps (type + coordinates)

## Default keys
- `J`: set goal from looked block
- `K`: build route to goal
- `L`: clear route
- `;`: aim to next route step
- `'`: toggle prebuilt route auto-run
- `O`: toggle live AI

## Notes
- Constants assume maxed AOTV-style simplicity:
  - Transmission range `12`, cost `27`
  - Etherwarp range `61`, cost `108`
- If Hypixel stat assumptions change, edit `AotvConfig.java`.
