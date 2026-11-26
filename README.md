# Kelvin Wake Duck 🦆

A cartoon simulator for the **Kelvin wake angle**. Move the pointer and the duck follows it around the lake. Swim fast or slow: the V-shaped wake always opens at the same half-angle, arcsin(1/3) ≈ **19.47°**.

**Live:** https://a-nelas.github.io/kelvin-wake-angle/

## Controls

- **Move the pointer** (or touch and drag): the duck swims after it
- **🔊 / 🔇**: lake sounds on or off. Browsers start sound only after a click, tap or key press

A small white scale rides along behind the duck and spans only the wake's 39° opening. The outer side counts the half-angle from the centre line (0 → 19.5° each way). The inner side counts the full opening from edge to edge (0 → 39°).

## How the wake is drawn

A moving source makes deep-water waves travelling at angle θ to its path, with phase speed c = U cos θ. Their energy moves at the group speed c/2. Each point of the duck's recent path sends out waves in many directions. Points of equal phase are joined into crest lines. This is the classic stationary-phase construction, and it produces the transverse waves, the divergent waves and the cusps along the 19.47° line. It works for curved paths and changing speeds too.

To keep the cartoon readable, crest spacing never drops below about 85 px. This scales the pattern at slow speeds but does not change its shape or angle.

It is a single static `index.html` with no build step and no dependencies.
