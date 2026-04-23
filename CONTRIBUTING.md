# Contributing IR Profiles

Thank you for contributing to the VDA IR Profiles repository! Your contributions help other users control their devices.

## How to Contribute

### Option 1: Export from VDA IR Control (Recommended)

If you've learned IR codes using the VDA IR Control integration:

1. Open the VDA IR Control card in Home Assistant
2. Go to **My Profiles** tab
3. Click **Export for Contribution** on your profile
4. Copy the JSON output
5. Create a new file in the appropriate directory (see structure below)
6. Submit a Pull Request

### Option 2: Manual JSON Creation

1. Fork this repository
2. Create a new JSON file in the appropriate directory
3. Follow the schema below
4. Submit a Pull Request

## Directory Structure

Place your profile in the correct directory based on device type:

```
tv/{manufacturer}/{profile_id}.json
soundbar/{manufacturer}/{profile_id}.json
av_receiver/{manufacturer}/{profile_id}.json
cable_box/{manufacturer}/{profile_id}.json
streaming/{manufacturer}/{profile_id}.json
projector/{manufacturer}/{profile_id}.json
```

Use lowercase for directory and file names. Replace spaces with underscores.

## Profile Schema

```json
{
  "profile_id": "manufacturer_model_variant",
  "name": "Manufacturer Model Display Name",
  "manufacturer": "Manufacturer",
  "device_type": "tv",
  "protocol": "NEC",
  "bits": 32,
  "codes": {
    "power": "HEX_CODE",
    "power_on": "HEX_CODE",
    "power_off": "HEX_CODE",
    "volume_up": "HEX_CODE",
    "volume_down": "HEX_CODE",
    "mute": "HEX_CODE",
    "channel_up": "HEX_CODE",
    "channel_down": "HEX_CODE",
    "source": "HEX_CODE",
    "menu": "HEX_CODE",
    "enter": "HEX_CODE",
    "exit": "HEX_CODE",
    "up": "HEX_CODE",
    "down": "HEX_CODE",
    "left": "HEX_CODE",
    "right": "HEX_CODE",
    "back": "HEX_CODE",
    "home": "HEX_CODE",
    "0": "HEX_CODE",
    "1": "HEX_CODE",
    "2": "HEX_CODE",
    "3": "HEX_CODE",
    "4": "HEX_CODE",
    "5": "HEX_CODE",
    "6": "HEX_CODE",
    "7": "HEX_CODE",
    "8": "HEX_CODE",
    "9": "HEX_CODE"
  }
}
```

### Required Fields

- `profile_id` - Unique identifier (lowercase, underscores only)
- `name` - Human-readable display name
- `manufacturer` - Brand name
- `device_type` - One of: tv, soundbar, av_receiver, cable_box, streaming, projector
- `codes` - At least `power` command is required

### Optional Fields

- `protocol` - IR protocol (NEC, SAMSUNG, SONY, PIONEER, RC5, RC6, raw)
- `bits` - Protocol bit length (default: 32)
- `model` - Specific model number(s) this works with

### Common Command Names

Use these standardized command names when possible:

**Power:**
- `power` - Toggle power
- `power_on` - Discrete power on
- `power_off` - Discrete power off

**Volume:**
- `volume_up`
- `volume_down`
- `mute`

**Channel:**
- `channel_up`
- `channel_down`

**Navigation:**
- `up`, `down`, `left`, `right`
- `enter` or `select`
- `back`
- `exit`
- `menu`
- `home`
- `guide`
- `info`

**Playback:**
- `play`, `pause`, `play_pause`
- `stop`
- `rewind`, `fast_forward`
- `record`

**Input:**
- `source` or `input`
- `hdmi1`, `hdmi2`, `hdmi3`, `hdmi4`
- `input_tv`, `input_cd`, `input_tuner`

**Numbers:**
- `0` through `9`

## Finding IR Codes

If you don't have the codes, here are some resources:

- [Tasmota IR Codes](https://tasmota.github.io/docs/Codes-for-IR-Remotes/)
- [IRDB Database](https://github.com/probonopd/irdb)
- [Remote Central](https://www.remotecentral.com/cgi-bin/codes/)
- Manufacturer documentation

## Testing Your Profile

Before submitting:

1. Validate your JSON syntax (use a JSON validator)
2. Test the codes with your actual device if possible
3. Ensure the profile_id is unique

## Pull Request Guidelines

1. One profile per pull request (easier to review)
2. Include the device model in the PR title
3. Note if you tested with actual hardware
4. Include any quirks or notes about the device

## Questions?

Open an issue if you have questions about contributing.
