# Kelvin Wake Duck 🦆

A cartoon simulator for the **Kelvin wake angle**. Drag anywhere to lead the duck around the lake and watch its wake. Swim fast or slow: the waves get longer or shorter (λ = 2πv²/g), but the V-shaped wake always opens at the same half-angle, arcsin(1/3) ≈ **19.47°**.

**Live:** https://a-nelas.github.io/kelvin-wake-angle/

## Controls

- **Drag** to make the duck follow your pointer
- **📐 Protractor** (P): show or hide the square protractor
- **📌 Pin to duck** (L): lock the protractor onto the duck, or unpin it to drag it around. Turn it with the round handle or the mouse wheel (hold Shift for fine steps)
- **⏸ Freeze** (Space): stop the water so you can measure
- **🔊 Sound** (M): gentle lake ambience, made live with the Web Audio API
- **Double-click** or **Q**: quack

## How the wake is drawn

A moving source makes deep-water waves travelling at angle θ to its path, with phase speed c = U cos θ. Their energy moves at the group speed c/2. Each point of the duck's recent path sends out waves in many directions. Points of equal phase are joined into crest lines. This is the classic stationary-phase construction, and it produces the transverse and divergent waves and the cusps along the 19.47° line. It works for curved paths and changing speeds too.

It is a single static `index.html` with no build step and no dependencies.
