# GlassMatch – prototype

A clickable prototype of a tool for windscreen call-centre agents: enter the customer's **rego** (or VIN) and get the **exact windscreen part** to order, so fewer wrong windscreens are sent out.

**Try it:** https://eslamafifi83-beep.github.io/glassmatch-prototype/

## How it works

1. **Find the car.** Rego + state (or VIN) → make, model, variant, series, build date.
2. **Narrow it down.** Windscreens that don't fit the build date are ruled out automatically. The agent then asks the customer only the questions that still matter (ADAS camera, rain sensor, heated screen, acoustic, head-up display), or the customer sends a photo of the code printed on the glass.
3. **Confirm the part.** Part code, fitter notes (e.g. ADAS recalibration needed), and an order summary to copy.

Sample cars to try: `NSW CXA22B` (RAV4), `VIC 1QR7FT` (Corolla), `QLD 829KLM` (HiLux), `WA 1HGT520` (CX-5).

## Important

All cars, VINs, part codes and history notes are **illustrative sample data**. Nothing is connected to a real vehicle register or parts catalogue yet.

## Planned real data sources

- **Rego → VIN / vehicle:** NEVDIS via an approved broker (e.g. RedBook, Blue Flag, MotorWeb, AutoGrab, PlateAPI).
- **VIN → glass part:** a glass catalogue/Eurocode lookup service, or the company's existing parts catalogue.
- **Photo check:** AI reading of the glass marking to confirm the part.
- **Order history:** past mis-orders to flag risky models.
