# Home Assistant config

Declarative config for my Home Assistant install (LAN address 192.168.1.175).

## Layout

This mirrors Home Assistant's own config folders, so a Git pull into the config
directory puts each file where HA expects it.

```
blueprints/automation/<author>/     Blueprints HA loads from its Blueprints page
  dansmi-hub/ikea_bilresa_scroll_wheel_light_control.yaml

automations/<area>/                 Automation configs, one file per automation
  living_room/bilresa_all_lights.yaml
```

Blueprint paths in automations are relative to `blueprints/automation/`, so
`path: dansmi-hub/ikea_bilresa_scroll_wheel_light_control.yaml` points at the file above.

## Naming

- Files: lowercase, underscores, named after the device or job (`bilresa_scroll_wheel`, `bilresa_all_lights`).
- Folders: `<author>` for blueprints, `<room or area>` for automations.

## Notes

- Keep tokens and passwords out of git. `secrets.yaml` and `.env` are ignored.
- Home Assistant runtime state (`.storage/`, logs, databases) is ignored.
- Live automations on the HA box may differ from what's in git until they're re-applied.
