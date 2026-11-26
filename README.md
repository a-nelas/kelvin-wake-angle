# Kelvin Wake Duck 🦆

A cartoon simulator for the **Kelvin wake angle**. Move the pointer and the duck follows it around the lake. Swim fast or slow: the V-shaped wake always opens at the same half-angle, arcsin(1/3) ≈ **19.47°**.

**Live:** https://a-nelas.github.io/kelvin-wake-angle/

## Controls

- **Move the pointer** (or touch and drag): the duck swims after it
- **Speaker button**: lake sounds on or off. Browsers start sound only after a click, tap or key press

A small white scale rides along behind the duck while it swims (it fades out when the duck stops) and spans only the wake's 39° opening. The outer side counts the half-angle from the centre line (0 → 19.5° each way). The inner side shows the full opening, 39°.

## How the wake is simulated

The wake comes from linear deep-water wave theory (ω² = gk), solved by stationary phase for a moving pressure source:

- For every earlier moment on the duck's path, the waves visible now travel at angle θ to the duck's velocity back then, with phase speed c = U cos θ.
- They have moved c·τ/2 (the group speed times their age τ) from where the duck was, and carry phase gτ / (2U cos θ). Crests are where that phase is a whole number of turns.
- Wave strength follows the physics too. The duck's footprint is about 13 px across, so it barely makes waves shorter than itself (factor exp(−(kL)²/4)). Energy thins out as the waves spread, and crests are strongest along the cusp line.

So a slow duck makes short, faint waves and a fast duck long, strong ones, while on a straight run the crests always end on the 19.47° lines. Curving paths, speeding up and stopping all fall out of the same model. The wavelength is the real λ = 2πU²/g at every speed.

It is a single static `index.html` with no build step and no dependencies.
