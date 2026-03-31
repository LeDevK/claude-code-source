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
