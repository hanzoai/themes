# Hanzo themes

Theme presets for the coding harnesses `hanzo code` drives — in each tool's
**native** theme format (no binary patching).

## Claude Code (`claude/*.json`)

Claude loads custom themes from `~/.claude/themes/<name>.json` and selects one
via `theme: "custom:<name>"` in `~/.claude/settings.json`. Schema:

```json
{ "name": "Dracula", "base": "dark", "overrides": { "<colorKey>": "#rrggbb" } }
```

`base` is a built-in theme (`dark`/`light`) whose colors fill any key not in
`overrides`. `hanzo code claude` drops the selected preset into `~/.claude/themes`
and selects it automatically (default: `dracula`).

- **dracula** — the Dracula palette, Claude accent in signature purple `#bd93f9`.

## Codex / hanzo dev

Codex-rs harnesses (`codex`, `dev`) theme via `~/.codex/config.toml` — presets
land here as that lands.
