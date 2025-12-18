# Lighting Profiles

IR profiles for LED controllers, smart bulbs, and lighting systems.

## Structure

```
lighting/
├── rgb_led/
│   └── generic_rgb_44key.json
├── philips/
│   └── philips_hue_ir.json
└── led_strip/
    └── generic_led_strip.json
```

## Common Commands

- `power`, `power_on`, `power_off`
- `brightness_up`, `brightness_down`
- `color_red`, `color_green`, `color_blue`, `color_white`
- `color_yellow`, `color_cyan`, `color_magenta`, `color_orange`
- `mode_flash`, `mode_strobe`, `mode_fade`, `mode_smooth`
- `speed_up`, `speed_down`

## Note

Many IR LED controllers use the same codes. The "generic_rgb_44key" profile
covers the common 44-key RGB LED strip remotes widely available.
