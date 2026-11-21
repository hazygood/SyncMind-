# SyncMind
A note-taking and scheduling app designed for windows (currently). It includes multiple features such as notes, schedules, alarms, and more. No ads, and no need to pay for features. More features are continuously being developed. All data is saved locally, safe and secure.

A local-first Windows tray companion for **notes, calendar, schedule and alarms** —
plus a data-package theming system that can restyle the entire UI.

Everything lives in one JSON file on your machine. No account, no sync server,
no telemetry. The app only touches the network when you check for updates or
browse the skin store.

## Features

- **Notes** — multiple notebooks, Markdown, full-text search, trash, version history,
  import/export `.md`, drag-to-reorder notebooks
- **Calendar** — Chinese lunar calendar, solar terms and public holidays,
  adjustable density and type scale, four font sizes
- **Schedule** — recurrence rules, multi-day events, reminders that ring like alarms
  (snooze / dismiss / missed-item digest)
- **Alarms** — weekday repeat, snooze, dedicated always-on-top ring window
- **Themes** — 8 built-in palettes, or install skins that replace colours, wallpaper,
  panel materials, frames, dividers, decorations, icons and fonts
- **Skin store** — browse and install from a static index, verified by SHA-256
- **Updates** — ~600 KB asar hot-swap with rollback, no reinstall needed

## How it's built

Electron 45, plain JavaScript, no framework and no runtime dependencies.
`contextIsolation` + `sandbox` are on, the renderer is under a strict CSP, and skins
are pure data (JSON manifest + images + fonts) served through a custom `lxskin://`
protocol — nothing from a skin is ever executed.

Skins use a *role-based* manifest: instead of binding assets to fixed slots, a skin
describes each region (window / bar / panel / card / cell / chip / pop) with colours,
materials, frames and decorations.

## Status

Windows only, UI in Chinese. Current release: **v1.4.0**.
