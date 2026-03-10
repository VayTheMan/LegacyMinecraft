
# Minecraft Legacy
**Play Minecraft: Legacy Console Edition on PC with enhancements**


![Gameplay Screenshot](.github/TutorialWorld.png)

## Overview

This repository houses the reconstructed source for Minecraft: Legacy Console Edition (TU19 / v1.6.0560.0), modified to run natively on Windows with modern improvements while preserving the classic console experience.

## Quick Start

**Windows users** can grab the latest [automated build](https:). Download the `.zip` archive, extract to any folder, and launch `Minecraft.Client.exe`. Create a `username.txt` file in the same directory to set your player name.

## System Compatibility

- **Windows 10/11**: Fully supported for development and gameplay
- **macOS/Linux**: May function through compatibility layers (Wine/CrossOver) based on user reports, but this configuration isn't officially maintained

## Key Improvements

- Successfully compiles and runs under Visual Studio 2022 (Debug/Release configurations)
- Full keyboard & mouse controls implemented
- Native fullscreen mode (F11 toggle)
- V-Sync can be disabled (experimental)
- High-precision timing for smoother gameplay at high frame rates
- Automatically matches your display's native resolution
- Working LAN multiplayer with server discovery
- Persistent profile system via external text file

## Multiplayer Setup

The Windows build includes functional local network multiplayer:

- Hosted worlds broadcast automatically to your LAN
- Discoverable through the in-game server browser
- Standard TCP `25565` for game connections
- UDP `25566` for LAN discovery
- Manual server entry available
- Your `uid.dat` preserves identity across sessions

### Command Line Options

| Flag              | Function                                    |
|-------------------|---------------------------------------------|
| `-name <player>`  | Specify your character name                 |
| `-fullscreen`     | Start directly in fullscreen mode           |

Usage example:
```
Minecraft.Client.exe -name Alex -fullscreen
```

## Control Scheme

**Movement & Navigation**
- Walk: `W` `A` `S` `D`
- Jump/Fly up: `Space`
- Sneak/Fly down: `Shift` (hold)
- Sprint: `Ctrl` (hold) or double-tap `W`
- Perspective toggle: `F5`
- Fullscreen: `F11`
- Menu/Cancel: `Esc`

**Inventory & Items**
- Open inventory: `E`
- Crafting menu: `C` (navigate tabs with `Q`/`E`)
- Drop held item: `Q`
- Hotbar selection: `1`-`9` or mouse wheel
- Item use/place: Right mouse button
- Attack/destroy: Left mouse button

**Interface & Debug**
- Chat: `T`
- Player list/Host options: `TAB`
- HUD visibility: `F1`
- Debug overlay: `F3`
- Advanced debug menu: `F4`
- Console toggle: `F6`
- Tutorial prompts: `Enter` (accept), `B` (decline)

## Building from Source

### Visual Studio 2022 (Recommended)

1. Download and install [Visual Studio 2022 Community](https://aka.ms/vs/17/release/vs_community.exe)
2. Clone this repository
3. Open `MinecraftConsoles.sln`
4. Verify `Minecraft.Client` is the startup project
5. Choose **Debug** or **Release** configuration with **Windows64** platform
6. Build and run (F5)

### CMake Alternative

```powershell
cmake -S . -B build -G "Visual Studio 17 2022" -A x64
cmake --build build --config Debug --target MinecraftClient
```

For detailed compilation instructions, see [COMPILE.md](COMPILE.md).

## Current Limitations

- Only Windows builds are actively tested and supported
- Cross-platform compatibility is experimental at best
- Some original console features may behave differently on PC hardware

## Contributing

Interested in helping improve the project? Check out our [Contribution Guidelines](CONTRIBUTING.md) for current priorities, coding standards, and submission process.

## Support the Project

If you find this project valuable and want to support continued development, donations are appreciated:

**Bitcoin (BTC):** `bc1qxy2kgdygjrsqtzq2n0yrf2493p83kkfjhx0wlh`

**Litecoin (LTC):** `ltc1qxy2kgdygjrsqtzq2n0yrf2493p83kkfjhx0wlh`

**Monero (XMR):** `4AdUndefinedZxyzAddressPlaceholderPleaseReplaceWithRealXMRAddressHereForSecurity`