# BLACKRELAY_CONCEPT_001

## Status

Planned.

BlackRelay is intended to be a local-first workflow automation and routing tool for the Blackfong software ecosystem.

It is separate from BlackBus. BlackBus moves events. BlackRelay reacts to events.

## Core Purpose

BlackRelay watches for local events and triggers local actions.

Example:

```text
3000 saves a motion snapshot
↓
BlackRelay detects the new event or file
↓
BlackRelay routes it to QuietDrop
↓
BlackRelay creates/logs an alert for Nightwatch
```

## MVP

Start with folder watcher mode, then later add BlackBus subscription. The MVP should provide config, watch folders, classify file events, log relay activity to SQLite, print local alerts, and route through dry-run QuietDrop/Nightwatch adapters.

Planned commands: `blackrelay init`, `blackrelay watch`, `blackrelay status`, `blackrelay test-event`, `blackrelay routes`.

MVP storage: SQLite at `data/blackrelay.sqlite3` with relay event and route result records.

BlackRelay is not the event bus, OBEOS, DAISE, a cloud workflow product, or a GUI. It is a bounded local dispatcher.

Future integration may include BlackBus subscription, real QuietDrop/Nightwatch actions, shell/Python adapters, retries, failed-route queues, validation, and dry-run previews.

Checkpoint: 001
