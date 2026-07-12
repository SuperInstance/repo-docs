# gh-dungeons

## Intention
A procedurally generated roguelike dungeon crawler that turns your repos into a unique playable game — and can also turn **PLATO knowledge rooms** into playable dungeon levels!

## How It Works
Each PLATO room maps to a dungeon level:

| PLATO Concept | Dungeon Equivalent |
|--------------|-------------------|
| Room | Dungeon Level |
| Tile | Monster / Item |
| Tile Question | Item Description |
| Tile Answer | Monster Name / Loot |
| Room Name | Level Seed |

The room's tile count determines enemy difficulty and count. Questions and answers from tiles become the text content visible on floor tiles, creating a unique procedural background for each level.

## What It's For
- **BSP-tree dungeon generation** - procedurally created rooms and corridors
- **PLATO integration** - knowledge rooms become dungeon levels
- **Fog of war** - limited vision radius, explored areas stay visible
- **Enemy AI** - enemies chase you when in line of sight
- **Auto-attack** - automatically attack adjacent enemies
- **Stats tracking** - kills and levels cleared
- <mark>**And way, way, wa

## Who Would Use It
```bash
gh extension install SuperInstance/gh-dungeons
```

Or build from source:
```bash
git clone https://github.com/SuperInstance/gh-dungeons
cd gh-dungeons
go build -o gh-dungeons
```

## Language / Stack
Go

## Status Assessment
Documented with code examples and API references (160 line README).

## Honest Assessment
Moderately documented (160 lines) with some code or API docs. Real content, likely functional.

---
*Source: [GitHub - SuperInstance/gh-dungeons](https://github.com/SuperInstance/gh-dungeons)*
