# Kelvin Wake Duck 🦆

A cartoon simulator for the **Kelvin wake angle**. Drag anywhere to lead the duck around the lake. Swim fast or slow: the V-shaped wake always opens at the same half-angle, arcsin(1/3) ≈ **19.47°**.

**Live:** https://a-nelas.github.io/kelvin-wake-angle/

## Controls

- **Drag**: the duck follows your pointer
- **📐** (P): show or hide the wedge protractor
- **📌** (L): pin the protractor to the duck, or unpin it to drag it. Turn it with the round handle or the mouse wheel (hold Shift for fine steps)
- **⏸** (Space): freeze the water so you can measure
- **🔊** (M): lake sounds (water laps, drips, birds, paddling), made live with the Web Audio API
- **Double-click** or **Q**: quack

## How the wake is drawn

A moving source makes deep-water waves travelling at angle θ to its path, with phase speed c = U cos θ. Their energy moves at the group speed c/2. Each point of the duck's recent path sends out waves in many directions. Points of equal phase are joined into crest lines. This is the classic stationary-phase construction, and it produces the transverse waves, the divergent waves and the cusps along the 19.47° line. It works for curved paths and changing speeds too.

To keep the cartoon readable, crest spacing never drops below about 85 px. This scales the pattern at slow speeds but does not change its shape or angle.

It is a single static `index.html` with no build step and no dependencies.
