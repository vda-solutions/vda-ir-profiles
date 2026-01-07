# VDA IR Profiles

Community IR code profiles for the [VDA IR Control](https://github.com/vda-solutions/vda-ir-control) Home Assistant integration.

## About

This repository contains IR codes for various devices (TVs, soundbars, AV receivers, cable boxes, streaming devices). These profiles can be synced directly into your Home Assistant instance via the VDA IR Control integration.

## Using These Profiles

1. Open the VDA IR Control card in Home Assistant
2. Go to the **Profiles** tab
3. Click **Sync Community Profiles**
4. Select a community profile when creating a new controlled device

## Contributing

We welcome contributions! If you have IR codes for a device not listed here, please submit a pull request.

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed instructions.

## Profile Format

Each profile is a JSON file with the following structure:

```json
{
  "profile_id": "manufacturer_model",
  "name": "Manufacturer Model Name",
  "manufacturer": "Manufacturer",
  "device_type": "tv",
  "protocol": "NEC",
  "bits": 32,
  "codes": {
    "power": "20DF10EF",
    "volume_up": "20DF40BF",
    "volume_down": "20DFC03F"
  }
}
```

### Device Types

- `tv` - Televisions
- `soundbar` - Sound bars and audio systems
- `av_receiver` - AV receivers and amplifiers
- `cable_box` - Cable boxes, satellite receivers, DVRs
- `streaming` - Streaming devices (Apple TV, Fire TV, Roku, etc.)
- `projector` - Projectors
- `projector_screen` - Motorized projector screens (up/down/stop)
- `blu_ray` - Blu-ray and DVD players
- `gaming` - Game consoles with IR support
- `fan` - Ceiling fans, tower fans, portable fans
- `ac` - Air conditioners and HVAC units
- `lighting` - LED controllers and smart lighting

### Common Protocols

- `NEC` - Most common, used by LG, Vizio, TCL, Hisense, etc.
- `SAMSUNG` - Samsung TVs and soundbars
- `SONY` - Sony devices (uses 12, 15, or 20 bit codes)
- `PIONEER` - Pioneer AV receivers
- `RC5` / `RC6` - Philips protocol

## Directory Structure

```
vda-ir-profiles/
├── tv/                  # Televisions
│   ├── samsung/
│   ├── lg/
│   ├── sony/
│   └── ...
├── soundbar/            # Sound bars
├── av_receiver/         # AV receivers & amplifiers
│   └── pioneer/
├── cable_box/           # Cable/satellite boxes
│   └── directv/
├── streaming/           # Streaming devices
│   ├── roku/
│   ├── amazon/
│   └── apple/
├── projector/           # Projectors
├── projector_screen/    # Motorized projector screens
│   └── elite_screens/
├── blu_ray/             # Blu-ray/DVD players
├── gaming/              # Game consoles
├── fan/                 # Fans (ceiling, tower, etc.)
├── ac/                  # Air conditioners
└── lighting/            # LED controllers
```

## License

These IR codes are provided as-is for personal use. Most IR codes are freely available from manufacturer documentation and public databases.
