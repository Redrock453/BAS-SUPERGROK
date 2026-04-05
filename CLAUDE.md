# CLAUDE.md - BAS-SUPERGROK Project Context

## Project Overview

**BAS-SUPERGROK** is a tactical/portfolio demo project featuring a terminal-style UI that simulates a hybrid AI operations center. It's designed to showcase:
- Terminal-based interactive UI
- AI agent visualization
- Tactical/military aesthetic
- Ukrainian language (primary)

## Files

### index.html
Main file - self-contained HTML with embedded CSS and JavaScript. Contains:
- Matrix rain canvas effect
- Scanline overlay
- Real-time system clock
- Interactive terminal with commands
- Agent status cards
- Operation protocol cards
- Notification system

**Key Features:**
- Matrix rain effect (toggleable with `matrix` command)
- Terminal commands: help, status, agents, scan, ops, clear, whoami, time, neofetch, logs, network
- Keyboard shortcuts: Tab (help), Ctrl+L (clear), Arrow keys (history)
- Agent panel with status indicators
- Clickable operation cards
- Random system notifications

### README.md
Ukrainian language documentation with:
- Full translation to Ukrainian
- Feature descriptions
- Setup instructions
- Tech stack documentation

## Design System

**Colors:**
- `--camo-dark: #0a120a` - Background
- `--camo-green: #1e2d1e` - Camo pattern
- `--tactical-gold: #b3924d` - Gold accents
- `--night-vision: #00ff41` - Terminal green
- `--blood-red: #ff3333` - VICTORIA accent
- `--cyber-cyan: #00f7ff` - Info highlights
- `--warning-orange: #ff9500` - Warnings

**Fonts:**
- Orbitron (headings)
- Rajdhani (body)
- Share Tech Mono (terminal)

## Terminal Commands

| Command | Description |
|---------|-------------|
| help | Show all commands |
| status | System & agent status |
| agents | AI agent details |
| scan | Network scan |
| ops | Active operations |
| clear | Clear terminal |
| whoami | User info |
| time | System time |
| matrix | Toggle matrix effect |
| neofetch | System info |
| logs | Recent logs |
| network | Network status |

## Customization

### Adding New Commands
Add to the `commands` object in the script section:
```javascript
'command-name': {
    response: 'Response text or function',
    type: 'info|warning|error|system'
}
```

### Adding Project Responses
Add to `projectResponses` object:
```javascript
'keyword': 'Response text'
```

## Verification

Test with:
1. Open `index.html` in browser
2. Try all terminal commands
3. Check matrix rain effect
4. Click operation cards
5. Verify responsive design
6. Test keyboard shortcuts

## Security Notes

This is a DEMO/PORTFOLIO project only. Not for actual tactical use.
- No real API integrations
- All responses are hardcoded/local
- No actual data collection

## Deployment

Simply deploy `index.html` to any static hosting:
- GitHub Pages
- Netlify
- Vercel

No build step required - fully static.