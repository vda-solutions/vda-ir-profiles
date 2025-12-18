# Air Conditioner Profiles

IR profiles for air conditioners, mini-splits, and HVAC units.

## Structure

```
ac/
├── lg/
│   └── lg_mini_split.json
├── samsung/
│   └── samsung_wind_free.json
├── daikin/
│   └── daikin_inverter.json
├── mitsubishi/
│   └── mitsubishi_mr_slim.json
└── frigidaire/
    └── frigidaire_window_unit.json
```

## Common Commands

- `power`, `power_on`, `power_off`
- `temp_up`, `temp_down`
- `mode_cool`, `mode_heat`, `mode_fan`, `mode_dry`, `mode_auto`
- `fan_low`, `fan_medium`, `fan_high`, `fan_auto`
- `swing_on`, `swing_off`, `swing_toggle`
- `timer_on`, `timer_off`
- `turbo`, `quiet`, `sleep`
- `set_temp_XX` (specific temperature presets)

## Note

AC units often require complex IR codes that include temperature and mode state.
Some profiles may include preset combinations (e.g., `cool_72f_high`).
