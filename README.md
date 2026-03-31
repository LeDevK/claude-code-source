# Claude Code Source snapshot for security research

This repository mirrors a publicly exposed Claude Code source snapshot that became accessible on March 31, 2026 through a source map exposure in the npm distribution. It is maintained for educational, defensive security research, and software supply-chain analysis.

# Repository Scope
Claude Code is Anthropic's CLI for interacting with Claude from the terminal to perform software engineering tasks such as editing files, running commands, searching codebases, and coordinating workflows.

This repository contains a mirrored src/ snapshot for research and analysis.

Public exposure identified on: 2026-03-31
Language: TypeScript
Runtime: Bun
Terminal UI: React + Ink
Scale: ~1,900 files, 512,000+ lines of code

# How the Public Snapshot Became Accessible
Chaofan Shou (@Fried_rice) publicly noted that Claude Code source material was reachable through a .map file exposed in the npm package:
"Claude code source code has been leaked via a map file in their npm registry!"

— @Fried_rice, March 31, 2026
The published source map referenced unobfuscated TypeScript sources hosted in Anthropic's R2 storage bucket, which made the src/ snapshot publicly downloadable.

# Directory Structure
src/
├── main.tsx                 # Entrypoint orchestration (Commander.js-based CLI path)
├── commands.ts              # Command registry
├── tools.ts                 # Tool registry
├── Tool.ts                  # Tool type definitions
├── QueryEngine.ts           # LLM query engine
├── context.ts               # System/user context collection
├── cost-tracker.ts          # Token cost tracking
│
├── commands/                # Slash command implementations (~50)
├── tools/                   # Agent tool implementations (~40)
├── components/              # Ink UI components (~140)
├── hooks/                   # React hooks
├── services/                # External service integrations
├── screens/                 # Full-screen UIs (Doctor, REPL, Resume)
├── types/                   # TypeScript type definitions
├── utils/                   # Utility functions
│
├── bridge/                  # IDE and remote-control bridge
├── coordinator/             # Multi-agent coordinator
├── plugins/                 # Plugin system
├── skills/                  # Skill system
├── keybindings/             # Keybinding configuration
├── vim/                     # Vim mode
├── voice/                   # Voice input
├── remote/                  # Remote sessions
├── server/                  # Server mode
├── memdir/                  # Persistent memory directory
├── tasks/                   # Task management
├── state/                   # State management
├── migrations/              # Config migrations
├── schemas/                 # Config schemas (Zod)
├── entrypoints/             # Initialization logic
├── ink/                     # Ink renderer wrapper
├── buddy/                   # Companion sprite
├── native-ts/               # Native TypeScript utilities
├── outputStyles/            # Output styling
├── query/                   # Query pipeline
└── upstreamproxy/           # Proxy configuration
