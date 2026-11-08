# How a power MOSFET turns on and off

An interactive, presentation-style animation of power MOSFET switching in a clamped inductive load.
The MOSFET is drawn with its three parasitic capacitors (C<sub>GS</sub>, C<sub>GD</sub>, C<sub>DS</sub>) so you can watch
gate charge move in and out of them through the four stages of turn-on and turn-off, including the Miller plateau.

**Live demo:** https://warayutmachima007-hash.github.io/mosfet-switching-animation/

## What it shows
- Charge building and draining on each parasitic capacitor, with the voltage across it
- Gate current splitting between C<sub>GS</sub> and C<sub>GD</sub> (almost 100 % into C<sub>GD</sub> on the plateau)
- Load current moving between the MOSFET and the free-wheeling diode
- V<sub>GS</sub>, I<sub>D</sub> and V<sub>DS</sub> waveforms with V<sub>TH</sub> and the plateau marked

Controls: Play, or step stage by stage with Next / Back (keys: Space, ← →). Drag on the waveforms to scrub.

## Model
Waveforms are computed in the browser from the analytical model in the source below: square-law channel,
constant C<sub>GS</sub>, drain-voltage dependent C<sub>GD</sub>, ideal diode, no stray inductance.
Example device: 600-V trench U-MOSFET switching 10 A at 400 V with R<sub>G</sub> = 5 Ω.
Simulated turn-off times agree with the book's analytical values to within about 10–20 %.

## Source
B. J. Baliga, *Advanced Power MOSFET Concepts*, Springer, 2010, DOI 10.1007/978-1-4419-5917-1.
Sec. 3.10 (Inductive Load Turn-Off Characteristics, Figs. 3.43–3.45) and Sec. 2.6 (Gate Charge, Figs. 2.25–2.27).

Single self-contained `index.html`; no build step.
