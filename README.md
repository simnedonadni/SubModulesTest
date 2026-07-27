# FM + Breath Resonators (Pure Data)

Vanilla Pure Data patch: `fm_breath_resonators.pd`

## What it does

Combines three sound stages:

1. **FM synthesis** — modulator at `carrier × ratio`, depth set by mod index, then carrier oscillator
2. **Filtered breath noise** — high-passed noise through three offset bandpass bands, amplitude-modulated for turbulence
3. **Resonant filter bank** — three parallel resonant bandpasses (formant-like) with dry/wet mix

## How to play

1. Open `fm_breath_resonators.pd` in Pure Data (Vanilla or Pd-extended)
2. DSP turns on from `loadbang` (or click the **DSP** toggle)
3. Click **bang** for a short note, or enable **hold** to sustain
4. Blend **fm-level** and **breath-amt**, then shape with the three resonators and **filter-mix**

## Controls

| Section | Parameters |
|---|---|
| FM | carrier Hz, mod ratio, mod index, FM level |
| Breath | amount, center Hz, Q, turbulence rate |
| Resonators | res1–3 frequency + Q, filter dry/wet |
| Output | master volume, bang / hold gate |

No externals required — uses only stock Pd objects (`osc~`, `noise~`, `bp~`, `vline~`, etc.).
