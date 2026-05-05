# Blon Addon

Blon is a weak Meteor Client addon that provides utility modules, commands, and themes for enhanced Minecraft gameplay. This addon focuses on leveraging command block cores for numerous utilities.

## Features

- **13 Utility Modules**: From particle auras to schematic placers
- **8 Custom Commands**: For core management and automation
- **10 GUI Themes**: Including misc client themes
- **Core System**: Advanced command block manipulation for utilities

## Installation

1. Download the latest release JAR file
2. Place it in your `mods` folder
3. Restart your game or reload Meteor Client
4. Access modules in the "Blon" category

## Join the Discord to give suggestions:

https://discord.gg/5PFjMYh6SG

## Dependencies

- Fabric API
- Meteor Client
- Litematica (runtime dependency for schematic loading)

## License

This project is provided as-is for educational purposes.

## Core System

The Blon addon heavily utilizes a "core" system based on command blocks. The core consists of a large structure of command blocks that can be manipulated to execute various commands server-side. This allows for misc utilies.

### Setting up the Core

Use the `.core` command to spawn a core:
```
.core [width] [length] [height] [block]
```

Default: 16x16x32 with red_stained_glass

## Modules

### AntiCrash
**Description**: Anti-crash  system that prevents various types of client crashes from malicious packets, entities, and translations.

**Key Settings**:
- **Text Limiter**: Limits text sizes in chat, titles, boss bars, etc.
- **Translation Anti Crash**: Prevents crashes from malicious translation keys
- **Particle Limiter**: Limits particle speed and count per tick
- **Entity Limiter**: Limits entity count and removes invalid entities
- **Rendering Quality**: Controls rendering of light beams, structure overlays, etc.
- **Rate Limits**: Limits sounds and chat messages per tick
- **FPS Checker**: Disconnects or runs commands when FPS drops too low
- **Notifications**: Shows alerts when protections are triggered

### Auto...
**Description**: Spawns block display using the command block core.

**Key Settings**:
- **Placement Mode**: How to position the displays (Relative/Absolute)
- **Placement Offset**: Offset from base position
- **Player Name**: Name of player to teleport (for smooth movement)
- **Teleport Offsets**: X/Y/Z offsets for teleport position
- **Teleport Speed**: Speed of up/down movement

### ChatBubble
**Description**: Displays chat messages as floating text bubbles above players' heads.

### ForceGrab
**Description**: Grabs entities and moves them around using the Core. Middle Click or '[' to grab entities and control their position *throw is broken rn*.

**Key Settings**:
- **Distance**: How far to hold the entity
- **Tracer**: Draw particle line to target
- **Particle Type**: Type of particle for tracer
- **Throw Force**: Force when throwing grabbed entity

### ImageEggs
**Description**: Spawns images using text_display spawn eggs. Creates visual displays of images or text in the world.

**Key Settings**:
- **Render Mode**: Normal or overlapping text display
- **Billboard Mode**: How text is oriented (center, etc.)
- **Overlap Factor**: Fraction of line width to overlap
- **Position Mode**: OPERATOR or CREATIVE positioning

### LegitKillAura
**Description**: A kill aura that appears legitimate to anti-cheat systems *semi broken*.

### NoParticleSpamModule
**Description**: Blocks command block output messages in chat to reduce spam from core operations.

### ParticleAuraModule
**Description**: Geometric particle aura using the core. Creates various 3D shapes made of particles around the player.

**Key Settings**:
- **Particle Style**: Shape type (Cube, Sphere, etc.)
- **Particle Type**: Particle effect to use
- **Max Packets Per Tick**: Rate limiting
- **Rotation Speeds**: X/Y/Z axis rotation speeds
- **Quality**: Particle density multiplier
- **Radius**: Size of the shape
- **Translate/Rotate**: Position and orientation offsets

### PlayerRotatorModule
**Description**: Rotates players around you using the Core. Forces nearby players to orbit around your position.

**Key Settings**:
- **Max Players**: Maximum number of players to rotate
- **Radius**: Rotation radius
- **Speed**: Rotation speed

### SchematicPlacer
**Description**: Places schematics using the command block core. Loads and places large structures from schematic files.

**Key Settings**:
- **Schematic File**: Name of schematic file (without extension)
- **Placement Mode**: How to position the schematic
- **Placement Offset**: Offset from placement position
- **Packets Per Tick**: Commands per tick
- **Core Mode**: Command block execution mode
- **Ignore Air**: Don't place air blocks
- **Use Volume Optimization**: Use fill commands for performance

### SongPlayer
**Description**: Plays music datapacks through the core. Allows playing custom music tracks using Minecraft's function system.

**Key Settings**:
- **Datapack File**: Name of zip datapack file
- **Start Function**: Function to start playback
- **Volume**: Volume multiplier
- **Packets Per Tick**: Rate limiting
- **Batch Size**: Commands per batch
- **Show Progress**: Display playback progress
- **Auto Schedule**: Follow schedule commands

### TotemBypass
**Description**: Bypasses totem protection using various methods including mace exploits. Allows killing players even when they have totem of undying.

**Key Settings**:
- **Weapon**: Weapon type (Mace)
- **Server Type**: Paper or Vanilla positioning
- **Fall Height**: Simulated fall height for power
- **Min/Max Height**: Height range for calculations
- **Delay Ticks**: Delay between packets
- **Check Obstacles**: Verify clear path before teleport
- **Attack Count**: Number of attacks per interaction
- **Auto Swap Back**: Return to previous item

### Pistol
**Description**: Shoots and kills players or breaks blocks using the core system.

**Key Settings**:
- **Range**: Maximum distance the pistol can shoot
- **Particle**: Particle to spawn on shot
- **Max Packets Per Tick**: Maximum number of C2S packets sent per tick
- **Gun Model**: Render the custom pistol model
- **Gun X/Y/Z**: Offsets for the gun model
- **Kill Sound/Break Sound**: Sounds played when killing/breaking
- **Sound Pitch**: Pitch of the pistol sounds

### PortalGun
**Description**: Creates portals using particles and the Command Block Core. Left click places blue portal, right click places orange portal. Walk into one to teleport to the other.

**Key Settings**:
- **Range**: Maximum distance to place portals
- **Height/Width**: Dimensions of the portal
- **Density**: Particle density multiplier
- **Teleport Trigger/Offset**: Distance to trigger teleport and offset destination
- **Gun Model**: Render the custom portal gun model
- **Gun X/Y/Z**: Offsets for the gun model

## Commands

### .ad
**Description**: Executes ad tellraw command in the first core impulse block (always active). Used for advertising our discord.

### .core
**Description**: Spawns a core with custom dimensions. Usage: `.core [w] [l] [h] [block]`

**Parameters**:f
- `w`: Width (default: 16)
- `l`: Length (default: 16)
- `h`: Height (default: 32)
- `block`: Block type (default: red_stained_glass)

### .function
**Description**: Controls the MCFunction player. Aliases: func, play

### .k
**Description**: Kills all entities except players.

### .loop
**Description**: Creates command loops for repeated execution.

### .particle-select
**Description**: Selects a particle type for use with ParticleAura module.

### .steal-inventory
**Description**: Steals items from containers or players.

### .testupdater
**Description**: Tests sending command block update packets using CoreUpdater methods.

**Usage**: `.testupdater <mode> <command>`

## Themes

Blon includes several GUI themes that mimic popular Minecraft clients:

- **Aristois**
- **Blon**
- **BlonGuiTheme**
- **Boze**
- **Fih (w fih client)**
- **Forest**
- **GlossyPurple**
- **Mercury**
- **Sigma**
- **ThunderHack**

## Contributing

I encourage you to work on this project and submit pull requests :D.

This addon is developed by blon (aka gerog).
