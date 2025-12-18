# Gaming Console Profiles

IR profiles for game consoles with IR receivers.

## Structure

```
gaming/
├── xbox/
│   └── xbox_media_remote.json
├── playstation/
│   └── ps5_media_remote.json
└── nintendo/
    └── nintendo_switch.json
```

## Common Commands

- `power`, `power_on`, `power_off`
- `up`, `down`, `left`, `right`, `select`
- `back`, `menu`, `home`
- `play`, `pause`, `stop`
- `rewind`, `fast_forward`
- `volume_up`, `volume_down`, `mute`

## Note

Many modern gaming consoles use Bluetooth or RF remotes rather than IR.
Only consoles with IR receivers or official IR media remotes are supported.
