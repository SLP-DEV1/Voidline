# Voidline CS2

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Status](https://img.shields.io/badge/status-active-green.svg)
![Platform](https://img.shields.io/badge/platform-windows-red.svg)
![Language](https://img.shields.io/badge/language-C%23-purple.svg)

**Voidline** is an external, memory-based utility framework for Counter-Strike 2 built with C# .NET 9.0 and a modern ImGui-based GUI. It leverages **ClickableTransparentOverlay** for rendering and provides a comprehensive collection of visualization and automation tools.

> **VAC & VAC Live Secure** — This project is designed to operate externally without injecting into the game process, avoiding known VAC and VAC Live detection vectors.

---

## ⚠️ Disclaimer

> This project is provided for educational and research purposes only. Usage in online games may result in account bans. The author assumes no responsibility for misuse.

---

## 📋 Features

### 🎯 Aimbot

Comprehensive aim-assist system with highly configurable options.

| Feature | Description |
|---------|-------------|
| **Bone Targeting** | Selectable hitbox: Head, Neck, Shoulders, Waist, Random |
| **FOV Circle** | Visible field-of-view circle with configurable radius and RGB color support |
| **Smoothing** | Independent X and Y smoothing values for smooth camera movement |
| **Keybind Support** | Fully customizable (default: MMB) |
| **Scoped-Only Mode** | Aimbot activates only when scoped |
| **Visibility Check** | Ray-triangle intersection via KD-Tree for wall visibility detection |
| **AutoWall Penetration** | Calculates damage through walls before firing |
| **Target Line** | Visual overlay line from player to target |
| **Backtrack Support** | Applies historical bone positions for improved hit registration |

---

### 🔫 TriggerBot

Automatic shooting system based on crosshair detection.

| Feature | Description |
|---------|-------------|
| **Crosshair-Based Detection** | Automatically detects enemies in crosshair |
| **Configurable Delay** | Minimum and maximum delay between shots |
| **Team Check** | Optional teammate shooting toggle |
| **Backtrack Integration** | Uses historical bone data for better hit registration |
| **AutoWall Penetration** | Only fires if the shot will deal sufficient damage |
| **Hitchance Calculation** | Calculates hit probability (0-100%) |
| **Punch Compensation** | Reduces recoil via counter mouse movement |
| **Configurable Trigger Key** | Fully customizable (default: MButton) |

---

### 🛡️ AutoWall

Advanced penetration system for wallbang shots.

| Feature | Description |
|---------|-------------|
| **Weapon Database** | 38+ weapons with base damage and penetration values |
| **CS2 Damage Formula** | Implements internal CS2 damage calculation |
| **Range Modifier** | 0.98 per distance unit |
| **Ray-Triangle Intersection** | Möller-Trumbore algorithm for wall detection |
| **Material System** | Accounts for wall materials (wood, concrete, metal, etc.) |
| **Multi-Penetration** | Calculates bullet penetration through multiple walls |

---

### 🎮 RCS - Recoil Control System

Automatic recoil compensation.

| Feature | Description |
|---------|-------------|
| **Strength Multiplier** | Stepless control from 0.0 to 1.0 |
| **AimPunchAngle Reading** | Reads current recoil angles from game memory |
| **Counter Movement** | Applies opposite mouse movement |
| **Keybind Check** | Activatable via configurable key (default: LMB) |
| **Shot Reset** | Resets on each new shot |

---

### 📊 Hitchance

Hit probability calculation system.

| Feature | Description |
|---------|-------------|
| **Accuracy Penalty Reading** | Reads weapon accuracy penalty directly from game |
| **Inaccuracy Model** | Accounts for standing, crouching, and movement |
| **Velocity Penalty** | Factors in player speed accuracy reduction |
| **Aim Punch Factor** | Incorporates current recoil into calculation |
| **Spread Cone Calculation** | Calculates spread cone radius at target distance |
| **Target Size Comparison** | Compares spread cone to target hitbox size |
| **Visibility Bonus** | 10% bonus for visible targets |
| **0-100% Output** | Percentage-based hit probability |

---

### 🐇 Bhop

Automatic bunny hop.

| Feature | Description |
|---------|-------------|
| **Auto Jump** | Automatically jumps while moving |
| **Keybind Support** | Fully customizable (default: Space) |
| **Memory Write** | Direct memory write for reliable execution |

---

### 🎮 FovChanger

Custom field of view modification.

| Feature | Description |
|---------|-------------|
| **Custom FOV Value** | Configurable FOV value (default: 60) |
| **Scoped Skip** | Does not activate when scoped |

---

### 💥 HitStuff

Visual and audio feedback on hits.

| Feature | Description |
|---------|-------------|
| **Hit Sounds** | Selectable sounds: NeverLose, Skeet |
| **Headshot Text Overlay** | Animated text with sine wave effect and fade |
| **Volume Control** | Configurable sound volume |
| **Custom Text Color** | Custom text color for hit notifications |
| **Headshot Counter** | Tracks and displays headshot count |

---

### 👁️ Chams

3D player hitbox visualization.

| Feature | Description |
|---------|-------------|
| **3D Hitbox Capsules** | Renders hitboxes as 3D capsules |
| **Team/Enemy Colors** | Separate color configuration for team and enemies |
| **Visible/Occluded** | Different colors for visible and hidden targets |
| **RGB Mode** | Animated RGB colors for all color options |
| **KD-Tree Visibility** | Precise visibility checking via wall geometry |
| **Bone Thickness** | Configurable capsule thickness |

---

### ⏱️ Backtrack Chams

Visualization of historical bone positions.

| Feature | Description |
|---------|-------------|
| **Historical Bones** | Displays bone positions from LagRecords |
| **Skeleton Overlay** | 19 bone connections rendered as line skeleton |
| **Configurable Colors** | Team/visibility-based color scheme |
| **Bone Radius Sizing** | Adjustable bone sizes |

---

### 🗺️ WorldESP

World entity visualization.

| Feature | Description |
|---------|-------------|
| **Chicken ESP** | ESP boxes for chickens |
| **Weapon ESP** | ESP for dropped weapons |
| **Projectile ESP** | ESP for grenades, smokes, etc. |
| **Hostage ESP** | ESP for hostages |
| **Molotov Bounds** | Fire circle rendered as convex hull |
| **3D Box Rendering** | Full bounding box ESP |
| **Text Labels** | Entity name text overlays |

---

### 📦 BoxESP

Versatile ESP box system with 9 shapes.

| Feature | Description |
|---------|-------------|
| **9 Box Shapes** | 2D Box, 3D Box, Edges, Pyramid, Star of David, Hexagon, Rhombus, Pentagram, Pentagon |
| **Team/Enemy Colors** | Separate color schemes |
| **Fill Option** | Optional box fill |
| **Gradient Support** | Color gradients |
| **Inner/Outer Outline** | Configurable outline styles |
| **Glow Effect** | Glow renderer integration |
| **Occluded Colors** | Different colors for visible/hidden targets |
| **Flash Check** | Visual indicator when flashed |

---

### 📍 Tracers

Lines from screen edges to players.

| Feature | Description |
|---------|-------------|
| **Start Positions** | Middle, Bottom, or Top of screen |
| **End Positions** | Bottom of screen or top of ESP box |
| **Team/Enemy Colors** | Separate color schemes |
| **Line Thickness** | Configurable line width |
| **Flash Check** | Indicator when flashed |

---

### 🔊 SoundESP

Visual representation of player audio proximity.

| Feature | Description |
|---------|-------------|
| **Expanding Circles** | Circles drawn when players make sounds |
| **Configurable Lifetime** | Maximum display duration (default: 1.5s) |
| **Configurable Radius** | Maximum circle size |
| **Team/Enemy Colors** | Separate color schemes |
| **RGB Support** | Animated RGB mode |

---

### 🎥 ThirdPerson

Switches to third-person camera perspective.

| Feature | Description |
|---------|-------------|
| **Memory Patch** | Patches JNE to JMP for third-person disable |
| **Camera Distance** | Configurable camera distance |

> ⚠️ **Warning:** Third-person may be detectable and can result in a ban.

---

### 💣 GrenadeLineup

Grenade lineup helper tool.

| Feature | Description |
|---------|-------------|
| **Save/Load System** | JSON-based lineup storage |
| **Lineup Types** | Still, Running, Jump, Run-Jump |
| **Position Circles** | Inner and outer positioning circles |
| **Angle Circles** | Displays aim angle indicators |
| **Click-to-Lock** | Click to lock aim direction |
| **Map-Specific Storage** | Separate lineups per map |
| **Always-Show Mode** | Display all lineups simultaneously |

---

### 👁️ SpectatorList

Shows who is spectating your player.

| Feature | Description |
|---------|-------------|
| **Observer Reading** | Reads observer target from dead players |
| **Spectator Names** | Displays spectator names |

---

### 🗺️ Radar

Mini radar overlay.

| Feature | Description |
|---------|-------------|
| **Render Range** | Configurable radar radius |
| **Proportion Scaling** | Maintains aspect ratio |
| **Point Types** | Circle, Arrow, Arc |
| **Team/Enemy Colors** | Separate color schemes |
| **Team Draw Toggle** | Show/hide teammates |
| **Crosshair Overlay** | Shows own view direction |
| **Yaw Rotation** | Points rotate based on player view direction |

---

### 🏷️ PingDisplay

Displays player ping values.

| Feature | Description |
|---------|-------------|
| **Player Ping** | Shows ping next to ESP boxes |

---

### ✨ NoFlash

Removes flashbang effect.

| Feature | Description |
|---------|-------------|
| **Anti-Flash** | Sets m_flFlashBangTime to 0 |

---

### 🏷️ NameDisplay

Displays player names.

| Feature | Description |
|---------|-------------|
| **Player Names** | Shows names above ESP boxes |

---

### ❤️ HealthBar

Visual health overlay.

| Feature | Description |
|---------|-------------|
| **Width Control** | Configurable bar width |
| **Rounded Corners** | Rounded corner styling |
| **Health Gradient** | Automatic color: Green → Yellow → Red |
| **RGB Mode** | Animated RGB health color |
| **Draw-On-Self** | Toggle own health bar visibility |

---

### 🚩 Flags

Visual status indicators.

| Feature | Description |
|---------|-------------|
| **Scoped Flag** | Shows when player is scoped |
| **Flashed Flag** | Shows flash duration with timer |
| **Weapon Icon** | Weapon-specific Unicode character |

---

### 👁️ EyeRay

Shows enemy view direction.

| Feature | Description |
|---------|-------------|
| **Enemy Eye Direction** | Line from enemy head showing look direction |

---

### 📏 DistanceText

Displays distance to players.

| Feature | Description |
|---------|-------------|
| **Distance Display** | Distance in meters below ESP boxes |

---

### 💣 C4ESP

Planted C4 visualization.

| Feature | Description |
|---------|-------------|
| **3D Box Around C4** | Bounding box around planted C4 |
| **Text Label** | C4 status as text |

---

### 🦴 BoneESP

Complete skeleton ESP system.

| Feature | Description |
|---------|-------------|
| **Straight Lines** | Standard bone connections |
| **Bezier Curves** | Smooth curved bone connections |
| **Team/Enemy Colors** | Separate visible/occluded colors |
| **Glow Effect** | Glow renderer integration |
| **Team Check** | Toggle teammate bones visibility |
| **Configurable Thickness** | Configurable line width |
| **19 Bone Connections** | Full skeleton |
| **Head Circle** | Circle highlight around head bone |

---

### 💣 BombTimerOverlay

C4 timer overview.

| Feature | Description |
|---------|-------------|
| **Planted Status** | Shows if C4 is planted |
| **Explosion Countdown** | Timer until detonation |
| **Bomb Site** | Shows A or B site |
| **Defuse Status** | Shows if C4 is being defused |

---

### 🛡️ ArmorBar

Visual armor overlay.

| Feature | Description |
|---------|-------------|
| **Width Control** | Configurable bar width |
| **Rounded Corners** | Rounded corner styling |
| **RGB Mode** | Animated RGB armor color |
| **Draw-On-Self** | Toggle own armor bar visibility |

---

## 🏗️ Architecture

### Core Components

| Component | Description |
|-----------|-------------|
| **Memory Manager** | kernel32.dll ReadProcessMemory/WriteProcessMemory wrapper for all data types |
| **Lag Compensation** | Stores position, rotation, eyeAngles, and 102-bone matrix per record (max 0.2s) |
| **MapLoader** | KD-Tree construction with parallel building and Möller-Trumbore ray-triangle intersection |
| **Visibility Check** | KD-Tree based wall visibility with m_bSpotted fallback |
| **Config System** | JSON-based save/load for all settings (Documents/Voidline/CS2/External/Configs/) |

### Rendering Engine

| Renderer | Functions |
|----------|-----------|
| **ShapeRenderer** | 3D circles, spheres, capsules, convex hulls, gradient rectangles |
| **GlowRenderer** | Multi-layer glow for rectangles, lines, circles, text, bezier curves |
| **TextRenderer** | Gradient text with animation |

### Data Structures

| Structure | Description |
|-----------|-------------|
| **Entity** | Position, bones, health, team, armor, weapons, animation, bomb data, hitboxes |
| **GameState** | Client/server addresses, localPlayer, entityList, viewMatrix |
| **LagRecord** | simulationTime, boneMatrix (102×8 floats), position, rotation, eyeAngles |
| **Hitbox** | Name, bounds (min/max), shapeRadius, boneMapping |
| **Bone** | Position, rotation (quaternion), visibility, transform matrix |

---

## 🖥️ GUI

The modern ImGui-based user interface is organized into four main categories:

### Aim
- Aimbot configuration (bone, FOV, smoothing, keybind, visibility, AutoWall)
- RCS / Recoil Control System
- TriggerBot settings (delay, teamCheck, backtrack, hitchance)

### Visuals
- **Box:** Shape selector, colors, fill, gradient, outline, glow, occluded
- **Player:** Chams, name, healthBar, armorBar, flags, eyeRay, distance, ping
- **Skeleton:** BoneESP, BacktrackChams, colors, thickness, glow
- **Tracers:** Start/end positions, colors, thickness
- **World:** Chicken, weapons, projectiles, hostages, molotov
- **Extras:** ThirdPerson, NoFlash, Radar, SpectatorList, C4ESP, BombTimer

### Legit
- **Profiles:** Config save/load
- **Movement:** Bhop, JumpShot, FOVChanger
- **Feedback:** HitSounds, HeadshotText, volume, color
- **Grenades:** Lineup save/load, types, positions
- **Interface:** GUI settings, colors, fonts
- **Performance:** Thread timing, FPS settings

### Settings
- GUI: Window position, size, theme
- Performance: Thread count, update intervals
- About: Version, credits, links

---

## 🛠️ Technology Stack

| Technology | Usage |
|------------|-------|
| **C# .NET 9.0** | Programming language and framework |
| **ImGuiNET** | GUI rendering |
| **ClickableTransparentOverlay** | Overlay rendering engine |
| **Newtonsoft.Json** | Config serialization |
| **System.Runtime.InteropServices** | Memory read/write operations |
| **System.Threading** | Asynchronous module execution |

---

## 📁 Project Structure

```
Voidline/
├── Classes/                    # Core components
│   ├── Memory.cs              # Memory read/write engine
│   ├── LagCompensation.cs     # Lag record system
│   ├── Configs.cs             # Config save/load
│   ├── VisibilityCheck.cs     # KD-Tree ray tracing
│   ├── Math/                  # Math utilities & calculations
│   └── Rendering/             # Shape, glow, text renderers
├── Modules/                   # Cheat modules
│   ├── Rage/                  # Aimbot, RCS, TriggerBot, AutoWall, Hitchance
│   ├── Legit/                 # Bhop, FOVChanger, HitStuff
│   └── Visual/                # Chams, ESP, Tracers, Radar, ...
├── Data/                      # Data structures
│   ├── Entity/                # Entity, Bone, Hitbox, LagRecord
│   ├── Game/                  # GameState, Offsets, MapParser
│   └── Types/                 # BombSite, VRF structures
├── ImGUI/                     # GUI components
│   ├── Theme/                 # MenuTheme, colors, styling
│   ├── Navigation/            # MenuNavigation, sidebar
│   ├── Pages/                 # AimPage, VisualsPage, LegitPage
│   └── Models/                # MenuCategoryInfo
├── Renderer.cs                # Main renderer & frame loop
└── Program.cs                 # Entry point
```

---

## 🔧 Requirements

- **OS:** Windows 10/11
- **.NET:** .NET 9.0 Runtime
- **Language:** C# 12
- **CS2:** Latest version of Counter-Strike 2

---

## 📜 License

This project is provided for educational purposes only. No warranty for functionality or security.

---

## 🙏 Credits

- **ClickableTransparentOverlay** — Overlay rendering framework
- **ImGuiNET** — C# binding for Dear ImGui
- **CS2 SDK** — Counter-Strike 2 offsets and structures

---

## 📢 Notice

This project is a utility framework for learning and demonstration purposes. Usage in multiplayer games may result in account bans. Use at your own risk.

**VAC & VAC Live Secure** — Designed to operate externally without injecting into the game process.
