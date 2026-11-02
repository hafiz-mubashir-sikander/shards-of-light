# Shards Of Light — High-Level Architecture

The diagram is a **conceptual overview** of the shipped game, not an export of proprietary implementation.

```text
                  ┌──────────────────────┐
                  │  Unity 6 / C# Game   │
                  └──────────┬───────────┘
                             │
           ┌─────────────────┼─────────────────┐
           │                 │                 │
    ┌──────▼──────┐   ┌──────▼──────┐   ┌──────▼──────┐
    │ Gameplay    │   │ Presentation│   │ Progression │
    │ Controls    │   │ UI / Audio   │   │ Local Saves │
    │ Enemies     │   │ Cutscenes    │   │ Stars/Levels│
    └──────┬──────┘   └──────┬──────┘   └──────┬──────┘
           └─────────────────┼─────────────────┘
                             │
                    ┌────────▼────────┐
                    │ Android Runtime │
                    └─────────────────┘
```

## Gameplay Layer

Movement, jumping, ladder and rope interactions, enemy encounters, damage, checkpoints, environmental hazards, collectibles, and boss phases.

## Level & Progression Layer

Seven levels, per-category collectible completion, three-star ratings, local level unlocks, and saved results.

## Presentation Layer

2D rendering through URP, animation, camera sequences, Timeline cutscenes, sound effects, background music, menus, and feedback.

## Optional Connected Services

AdMob ads and Google Play platform integrations may use network connectivity. Core gameplay and local progress do not depend on account registration.

## Private Implementation

Source code, Unity scenes/prefabs, asset pipelines, internal settings, third-party licensed files, release signing, and production service configuration are intentionally omitted.
