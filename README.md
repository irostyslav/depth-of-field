# Depth of Field Simulator

Interactive photography tool for exploring how **aperture**, **focal length**, **subject distance**, and **sensor size** change depth of field.

Live demo: https://irostyslav.github.io/depth-of-field/

Inspired by the simulator popularized in photography / #pctips reels (original reference: [jherr/depth-of-field](https://github.com/jherr/depth-of-field)). This is an original implementation with the same optical model.

## What you can do

- Drag **distance**, **focal length**, and **aperture** sliders
- Switch **metric / imperial** units
- Change **sensor** (phone, APS-C, full frame, medium format, …)
- Swap **subjects** and jump to **quick presets**
- Jump focus to the **hyperfocal** distance
- See near focus, far focus, total DoF, and the light cone in the scene

## Optical model

All distances internally use millimeters.

- Circle of confusion is derived from the sensor diagonal (Zeiss-style ≈ diagonal / 1500)
- Hyperfocal H = f² / (N · c) + f
- Near limit Dn = s(H - f) / (H + s - 2f)
- Far limit Df = s(H - f) / (H - s) (infinite when s ≥ H)

## Local use

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8080
```

## License

MIT
