# ⚔️ Enshrouded Dedicated Server Config Editor

<div align="center">

```svg
<svg width="800" height="200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="goldGradient" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#d4af37;stop-opacity:1">
        <animate attributeName="stop-color" values="#d4af37;#e67e22;#d4af37" dur="3s" repeatCount="indefinite"/>
      </stop>
      <stop offset="100%" style="stop-color:#e67e22;stop-opacity:1">
        <animate attributeName="stop-color" values="#e67e22;#d4af37;#e67e22" dur="3s" repeatCount="indefinite"/>
      </stop>
    </linearGradient>

    <filter id="glow">
      <feGaussianBlur stdDeviation="3.5" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <linearGradient id="flameGradient" x1="0%" y1="100%" x2="0%" y2="0%">
      <stop offset="0%" style="stop-color:#e67e22;stop-opacity:1"/>
      <stop offset="50%" style="stop-color:#e74c3c;stop-opacity:0.8"/>
      <stop offset="100%" style="stop-color:#f39c12;stop-opacity:0.3"/>
    </linearGradient>
  </defs>

  <!-- Castle Silhouette -->
  <rect x="50" y="120" width="80" height="70" fill="#2a211a" opacity="0.8"/>
  <rect x="45" y="110" width="15" height="25" fill="#2a211a" opacity="0.8"/>
  <rect x="120" y="110" width="15" height="25" fill="#2a211a" opacity="0.8"/>
  <polygon points="55,110 70,95 85,110" fill="#2a211a" opacity="0.8"/>
  <polygon points="100,110 115,95 130,110" fill="#2a211a" opacity="0.8"/>

  <rect x="670" y="120" width="80" height="70" fill="#2a211a" opacity="0.8"/>
  <rect x="665" y="110" width="15" height="25" fill="#2a211a" opacity="0.8"/>
  <rect x="740" y="110" width="15" height="25" fill="#2a211a" opacity="0.8"/>
  <polygon points="675,110 690,95 705,110" fill="#2a211a" opacity="0.8"/>
  <polygon points="720,110 735,95 750,110" fill="#2a211a" opacity="0.8"/>

  <!-- Animated Torches -->
  <rect x="160" y="140" width="8" height="40" fill="#5a4a38"/>
  <ellipse cx="164" cy="135" rx="10" ry="15" fill="url(#flameGradient)">
    <animate attributeName="ry" values="15;18;12;15" dur="1s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.8;1;0.7;0.8" dur="1s" repeatCount="indefinite"/>
  </ellipse>

  <rect x="632" y="140" width="8" height="40" fill="#5a4a38"/>
  <ellipse cx="636" cy="135" rx="10" ry="15" fill="url(#flameGradient)">
    <animate attributeName="ry" values="15;12;18;15" dur="1s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.8;0.7;1;0.8" dur="1s" repeatCount="indefinite"/>
  </ellipse>

  <!-- Crossed Swords -->
  <g transform="translate(200, 100)">
    <rect x="-3" y="0" width="6" height="60" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(-20 0 30)"/>
    <polygon points="0,-10 -8,0 8,0" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(-20 0 30)"/>
    <circle cx="0" cy="55" r="8" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(-20 0 30)"/>
  </g>

  <g transform="translate(600, 100)">
    <rect x="-3" y="0" width="6" height="60" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(20 0 30)"/>
    <polygon points="0,-10 -8,0 8,0" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(20 0 30)"/>
    <circle cx="0" cy="55" r="8" fill="url(#goldGradient)" filter="url(#glow)" transform="rotate(20 0 30)"/>
  </g>

  <!-- Main Title -->
  <text x="400" y="100" font-family="Georgia, serif" font-size="42" font-weight="bold" text-anchor="middle" fill="url(#goldGradient)" filter="url(#glow)">
    ENSHROUDED
    <animate attributeName="opacity" values="1;0.8;1" dur="2s" repeatCount="indefinite"/>
  </text>

  <text x="400" y="135" font-family="Georgia, serif" font-size="24" text-anchor="middle" fill="#b8a590">
    Server Configuration Editor
  </text>

  <!-- Decorative Line -->
  <line x1="250" y1="155" x2="550" y2="155" stroke="url(#goldGradient)" stroke-width="2" opacity="0.6">
    <animate attributeName="opacity" values="0.4;0.8;0.4" dur="3s" repeatCount="indefinite"/>
  </line>

  <!-- Subtitle -->
  <text x="400" y="180" font-family="Georgia, serif" font-size="16" font-style="italic" text-anchor="middle" fill="#d4af37" opacity="0.8">
    A Web-Based Tool for Dedicated Server Management
  </text>
</svg>
```

---

### 🏰 **Manage Your Realm with Ease** 🏰

A beautiful, browser-based configuration editor for Enshrouded dedicated servers.
No more manual JSON editing. No more syntax errors. Just pure server management.

[![License: MIT](https://img.shields.io/badge/License-MIT-gold.svg)](LICENSE)
[![Made with Love](https://img.shields.io/badge/Made%20with-%E2%9D%A4%EF%B8%8F-orange)](https://github.com)

</div>

---

## 📜 Table of Contents

- [Why This Tool Matters](#-why-this-tool-matters)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [How to Use](#-how-to-use)
- [Configuration Options](#-configuration-options)
- [Technical Details](#-technical-details)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Why This Tool Matters

Managing an **Enshrouded** dedicated server requires editing the `enshrouded_server.json` configuration file, which can be daunting for several reasons:

### The Problem
- **Complex JSON Structure**: The config file contains 30+ settings with nested objects and arrays
- **Syntax Errors**: One misplaced comma, missing quote, or bracket can break your entire server
- **Cryptic Values**: Settings like `fromHungerToStarving: 600000000000` (nanoseconds!) are not intuitive
- **User Groups Management**: The `userGroups` array is particularly tricky to edit manually
- **No Validation**: Text editors won't tell you if you've entered invalid values

### The Solution
This web-based editor provides:
- ✅ **Visual Interface**: Beautiful, themed UI matching Enshrouded's aesthetic
- ✅ **Error Prevention**: No more JSON syntax errors - the tool handles all formatting
- ✅ **Clear Labels**: Every setting has descriptions and valid ranges
- ✅ **Smart Conversion**: Automatically converts between user-friendly units (minutes) and technical units (nanoseconds)
- ✅ **Live Preview**: Sliders and toggles show exactly what you're configuring
- ✅ **Preset Support**: Quickly apply Default, Relaxed, Hard, or Survival difficulty presets
- ✅ **User Groups GUI**: Add, edit, and remove permission groups with ease

### Community Impact
According to community discussions and existing tools on platforms like Nexus Mods and GitHub, server administrators struggle with manual JSON editing. Similar tools have been created using Python with GUI frameworks, but this **browser-based solution** requires no installation, works on any platform, and provides a more accessible experience for server hosts who may not be technically inclined.

---

## ✨ Features

### 🎮 Comprehensive Settings Management
- **General Settings**: Server name, IP, ports, player slots
- **Player Stats**: Health, mana, stamina, body heat modifiers
- **Survival Mechanics**: Hunger, weapon durability, shroud time, tombstone modes
- **World Settings**: Day/night cycle, weather frequency, wildlife taming
- **Enemy Configuration**: Spawn rates, damage, health, aggression for both regular enemies and bosses
- **Resources & Crafting**: Mining effectiveness, plant growth, workstation speed, upgrade costs
- **User Groups & Permissions**: Password-protected groups with customizable access levels

### 🎨 Beautiful Medieval Theme
- Custom color scheme inspired by Enshrouded's atmosphere
- Smooth animations and transitions
- Responsive design for desktop and mobile
- Interactive sliders with real-time value display

### 💾 File Operations
- **Load Config**: Import existing `enshrouded_server.json` files
- **Save Configuration**: Download your edited config file
- **Export JSON**: Generate a properly formatted JSON file
- **Reset to Defaults**: Quickly restore official default settings

### 🛡️ Built-in Presets
- **Default**: Standard game balance (recommended for new players)
- **Relaxed**: Easier gameplay with more resources and fewer enemies
- **Hard**: Challenging experience with tougher, more numerous enemies
- **Survival**: Hardcore mode with hunger mechanics and aggressive enemies
- **Custom**: Full manual control over every setting

---

## 🚀 Quick Start

### Option 1: Local Use (No Server Required)
1. **Download** or clone this repository
2. **Open** `index.html` in any modern web browser
3. **Start configuring** your server settings
4. **Save** the generated `enshrouded_server.json` file

### Option 2: Host on a Web Server
1. Upload the `index.html` file to any web server
2. Access it via your browser
3. Share the URL with other server administrators

### Requirements
- Any modern web browser (Chrome, Firefox, Edge, Safari)
- No installation, no dependencies, no framework needed
- Works offline - all processing happens in your browser

---

## 📖 How to Use

### Step 1: Access the Editor
Open `index.html` in your web browser. You'll see the medieval-themed configuration interface.

### Step 2: Configure Your Server

#### General Settings Tab
- Set your **server name** (what players see in the server list)
- Configure **IP address** (usually `0.0.0.0` for public servers)
- Set **query port** (default: 15637)
- Adjust **player slots** (1-16 players)
- Enable/disable **text chat** and **voice chat**
- Choose **voice chat mode** (Proximity or Global)

#### Player Settings Tab
- Adjust player **health, mana, and stamina** (25%-400%)
- Configure **body heat** resistance to cold
- Enable/disable **weapon durability**
- Toggle **hunger & starvation** mechanics
- Set **food buff duration** and **hungry state duration**
- Modify **shroud time** (how long players can stay in the Shroud)
- Choose **tombstone mode** (what players lose on death)
- Set **shroud curse difficulty**
- Adjust **experience gain** for combat, mining, and exploration

#### World Settings Tab
- Configure **daytime duration** (2-60 minutes)
- Set **nighttime duration** (2-60 minutes)
- Choose **weather frequency** (Disabled/Rare/Normal/Often)
- Enable/disable **glider turbulences**
- Set **taming failure penalty** for wildlife

#### Enemy Settings Tab
- Set **enemy spawn amount** (Few/Normal/Many/Extreme)
- Configure **simultaneous attackers**
- Toggle **pacify all enemies** mode
- Adjust **enemy damage** (25%-500%)
- Modify **enemy health** (25%-400%)
- Set **enemy stamina** (stun resistance)
- Configure **enemy perception** range
- Adjust **attack frequency**
- Separately configure **boss damage** and **boss health** (20%-500%)

#### Resources & Crafting Tab
- Set **mining effectiveness** (damage and yield per hit)
- Adjust **resource gain** from loot and chests
- Configure **plant growth speed**
- Modify **workstation production speed**
- Set **weapon upgrade costs**
- Adjust **recycling yield** when salvaging upgraded weapons

#### User Groups Tab
- **View existing groups** (default: Admin, Friend, Guest)
- **Add new groups** with custom permissions
- **Edit permissions**:
  - Can Kick/Ban Players
  - Can Access Inventories (chests, containers)
  - Can Edit Base (modify existing structures)
  - Can Extend Base (build new structures)
  - Reserved Slots (guarantee spots for specific groups)
- **Set passwords** for each group
- **Remove groups** you don't need

### Step 3: Apply Preset (Optional)
Use the **Game Preset** dropdown in General Settings to quickly apply:
- **Default**: Official default settings
- **Relaxed**: Easier gameplay
- **Hard**: Challenging experience
- **Survival**: Hardcore mode

Note: Selecting a preset will override your custom settings (you'll be prompted to confirm).

### Step 4: Save Your Configuration

#### Option A: Load an Existing Config First
1. Click **"Load Config"**
2. Select your existing `enshrouded_server.json` file
3. The editor will populate all fields with your current settings
4. Make your changes
5. Click **"Save Configuration"** or **"Download JSON"**

#### Option B: Start from Scratch
1. Configure all settings using the tabs
2. Click **"Save Configuration"** to download `enshrouded_server.json`
3. Place the file in your Enshrouded server directory (same folder as `enshrouded_server.exe`)

### Step 5: Apply to Your Server
1. **Locate** your Enshrouded dedicated server folder
2. **Backup** your existing `enshrouded_server.json` (if any)
3. **Copy** the downloaded file to your server folder
4. **Restart** your Enshrouded dedicated server
5. **Verify** settings by checking the server logs

### Reset to Defaults
If you want to start over, click the **"Reset to Defaults"** button. This restores all official default values including the three default user groups (Admin, Friend, Guest).

---

## ⚙️ Configuration Options

### Server Information
| Setting | Description | Default |
|---------|-------------|---------|
| **name** | Server name displayed in browser | "Enshrouded Server" |
| **ip** | IP address to bind to | "0.0.0.0" |
| **queryPort** | Port for server queries | 15637 |
| **slotCount** | Maximum players | 16 |
| **saveDirectory** | Path to save files | "./savegame" |
| **logDirectory** | Path to log files | "./logs" |

### Game Settings
All game settings are documented in detail in the included `enshrouded_server_readme.txt` file, which contains the official documentation from the Enshrouded development team.

### User Groups
Each user group supports:
- **name**: Group identifier
- **password**: Required to join as this group
- **canKickBan**: Kick/ban other players
- **canAccessInventories**: Open chests and containers
- **canEditBase**: Modify existing structures
- **canExtendBase**: Build new structures
- **reservedSlots**: Guarantee slots even when "full"

---

## 🔧 Technical Details

### Technology Stack
- **Pure HTML/CSS/JavaScript**: No frameworks, no build process
- **Vanilla JavaScript**: No dependencies or external libraries
- **CSS Grid & Flexbox**: Responsive layout system
- **LocalStorage Ready**: Could be extended to save drafts locally

### Browser Compatibility
- ✅ Chrome/Edge 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Opera 76+

### File Structure
```
Enshrouded-Dedicated-Server-Config-Editor/
│
├── index.html                      # Main application (all-in-one file)
├── enshrouded_server_readme.txt    # Official documentation
├── README.md                       # This file
└── LICENSE                         # MIT License
```

### Key Features of the Code
- **Tab System**: Organized settings across 6 main categories
- **Slider Controls**: Real-time value updates with visual feedback
- **Toggle Switches**: Beautiful custom checkbox replacements
- **Form Validation**: Built-in min/max constraints
- **JSON Generation**: Properly formatted output with tabs
- **Preset System**: Pre-configured difficulty modes
- **Dynamic User Groups**: Add/remove groups on the fly

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Reporting Issues
- Check the config file generated matches expected format
- Report any bugs or unexpected behavior
- Suggest new features or improvements

### Submitting Changes
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Areas for Enhancement
- Add import/export for specific sections
- Include tooltips for all settings
- Add visual preset previews
- Create backup/versioning system
- Add validation warnings for unusual value combinations
- Support for multiple config file management

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### What This Means
- ✅ Use commercially
- ✅ Modify freely
- ✅ Distribute
- ✅ Private use
- ⚠️ Provide attribution
- ⚠️ Include license copy

---

## 🎮 About Enshrouded

**Enshrouded** is a survival action RPG developed by Keen Games. Players explore a vast voxel-based continent shrouded in deadly fog, building bases, crafting equipment, and battling enemies to survive.

This configuration editor is a **community-created tool** and is not officially affiliated with Keen Games or Enshrouded. It's designed to help server administrators manage their dedicated servers more easily.

---

## 🙏 Acknowledgments

- **Keen Games** for creating Enshrouded and providing detailed server documentation
- **Community Server Hosts** who identified the need for easier configuration tools
- **Existing Tool Creators** on Nexus Mods and GitHub who pioneered server config solutions
- **Contributors** who help improve this tool

---

<div align="center">

### ⚔️ **May Your Server Thrive** ⚔️

**Happy Hosting!**

---

*Built with ❤️ for the Enshrouded community*

</div>
