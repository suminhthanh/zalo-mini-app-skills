# Zalo Mini App Skill

Build Zalo Mini Apps - lightweight web apps running inside the Zalo super-app platform.

## Features

- **ZaUI Components** - Button, Input, Modal, Tabs, Avatar, Calendar, List, and 50+ more
- **JavaScript APIs** - authorize, getUserInfo, getPhoneNumber, getLocation, Storage, Camera
- **Checkout SDK** - Payment integration for Vietnamese market
- **Design Guidelines** - Colors, typography, spacing, icons following Zalo standards
- **Development Tools** - zmp-cli, VSCode extension, debugging

## Installation

### Option 1: Using add-skill CLI (Recommended)

```bash
# Install to current project
npx add-skill suminhthanh/zalo-mini-app-skills

# Install globally
npx add-skill suminhthanh/zalo-mini-app-skills -g

# Install for specific agent
npx add-skill suminhthanh/zalo-mini-app-skills -a claude-code
```

### Option 2: Manual Installation

**For Claude Code:**
```bash
# Clone to Claude Code skills directory
git clone https://github.com/suminhthanh/zalo-mini-app-skills.git
cp -r zalo-mini-app-skills/skills/zalo-mini-app ~/.claude/skills/
```

**For Project-level:**
```bash
mkdir -p .claude/skills
cp -r zalo-mini-app-skills/skills/zalo-mini-app .claude/skills/
```

### Option 3: Direct Download

```bash
# Download and extract
curl -L https://github.com/suminhthanh/zalo-mini-app-skills/archive/main.zip -o skill.zip
unzip skill.zip
cp -r zalo-mini-app-skills-main/skills/zalo-mini-app ~/.claude/skills/
```

## Supported Agents

| Agent | Skills Directory |
|-------|-----------------|
| Claude Code | `~/.claude/skills/` or `.claude/skills/` |
| Cursor | `~/.cursor/skills/` or `.cursor/skills/` |
| OpenCode | `~/.opencode/skill/` |
| GitHub Copilot | `.github/copilot/skills/` |
| Windsurf | `~/.windsurf/skills/` |

## Usage

Once installed, the skill activates automatically when you:

- Build new Zalo Mini Apps
- Use ZaUI components
- Call Zalo SDK APIs
- Integrate payments with Checkout SDK
- Follow Zalo design guidelines

### Quick Start

```bash
npm install -g zmp-cli
zmp create my-app && cd my-app && zmp start
```

### Example Prompts

- "Create a Zalo Mini App with bottom navigation"
- "Add user authentication using Zalo authorize API"
- "Implement a product list with ZaUI components"
- "Integrate Checkout SDK for payment"

## Skill Structure

```
zalo-mini-app/
├── SKILL.md                    # Main skill file
└── references/
    ├── getting-started.md      # Setup & deployment
    ├── api-overview.md         # API categories
    ├── api-user.md             # User APIs
    ├── api-storage.md          # Storage APIs
    ├── api-ui.md               # UI APIs
    ├── api-device.md           # Device APIs
    ├── api-zalo.md             # Zalo integration
    ├── zaui-overview.md        # Components overview
    ├── zaui-layout.md          # Layout components
    ├── zaui-display.md         # Display components
    ├── zaui-form.md            # Form components
    ├── zaui-overlay.md         # Overlay components
    ├── design-guidelines.md    # Design standards
    ├── web-design-guidelines.md # Accessibility, forms, animations, touch, i18n
    └── react-best-practices.md # Waterfalls, bundle size, re-renders, JS performance
```

## Related Projects

### zca-cli - Zalo CLI for Developers

<p align="center">
  <a href="https://zca-cli.dev">
    <img src="https://img.shields.io/badge/⚡_zca--cli-Automate_Zalo_Like_a_Pro-blue?style=for-the-badge&logo=terminal" alt="zca-cli"/>
  </a>
</p>

A powerful command-line interface for the Zalo messaging platform. Automate messaging, manage groups, and build custom integrations directly from your terminal.

**Features:**
- QR code login with multi-account support
- Send text, images, videos, voice messages, and stickers
- Group management (create, rename, add/remove members)
- Real-time message listener with webhook integration
- Batch operations and URL download support

**Quick Install:**
```bash
# macOS / Linux
curl -fsSL https://get.zca-cli.dev/install.sh | bash

# Windows (PowerShell)
irm https://get.zca-cli.dev/install.ps1 | iex
```

[Website](https://zca-cli.dev)

### Clawdbot - AI Agent with Zalo Integration

<p align="center">
  <a href="https://clawd.bot">
    <img src="https://img.shields.io/badge/🤖_Clawdbot-AI_Agent_Gateway-purple?style=for-the-badge" alt="Clawdbot"/>
  </a>
</p>

A powerful agentic AI assistant with multi-channel messaging support. The **Zalo User** channel uses `zca-cli` under the hood to automate personal Zalo accounts.

**Features:**
- Uses `zca listen` for receiving messages and `zca msg` for replies
- Text, media, and link messaging support
- Access control with pairing mode, allowlist, and group policies
- Multi-account support via zca profiles
- WebSocket gateway with tool execution and session management

[Documentation](https://docs.clawd.bot/channels/zalouser) | [Website](https://clawd.bot)

## Resources

- [Zalo Mini App Documentation](https://miniapp.zaloplatforms.com/documents/)
- [Mini App Center](https://miniapp.zaloplatforms.com/)
- [Agent Skills Specification](https://agentskills.io/specification)

## License

MIT
