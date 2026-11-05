# Changelog

## Unreleased

- Things defined in `.things` files now connect. The `httpServerUrl` property is set from
  `webServerAddress` when it is missing, instead of leaving the controller URL host null.
- `webServerAddress` accepts an `http://` or `https://` prefix (and a trailing `/json`).
- MAC address, firmware version and model properties are filled in for Things defined in files.
- Door and controller channels are set from the controller's status at startup, so items no longer
  show an old door state until the next UDP event.
- A rejected authorization token is reported as a token problem, not as an unreachable controller.
- The Thing stays OFFLINE when its configuration check fails, instead of going ONLINE anyway.
- Fixed a null-result error that logged an ERROR for every linked item when the controller
  rejected a request.
- The Thing comes back ONLINE by itself after a temporary communication error.
- Door Partial Open items no longer briefly change to 0 each time the Thing starts.

## 5.2.0 - 2026-10-12

- Builds against openHAB 5.2.0 (Java 21).
- License headers and static code analysis rules updated for openHAB 5.2.
- UDP status messages are decoded as UTF-8, and names are upper-cased with `Locale.ROOT`.
- New **Server Connection Monitoring** channel (`controller#serverMonitor`), from section 3.8 of the
  Local Control API (firmware 10.61 or later). UNDEF on older firmware.
- The **Firmware Version** channel (`controller#firmwareVersion`) now appears on the Thing.
- Both channels are added to existing iQ3 Things automatically.

## 4.2.3 - 2026-10-12

- Moved out of the openhab-addons fork (branch `tailwind`) into this repository,
  keeping the binding's git history.
- Builds on its own against the released openHAB 4.2.3 parent (Java 17).
- New **Server Connection Monitoring** channel (`controller#serverMonitor`), from section 3.8 of the
  Local Control API (firmware 10.61 or later). UNDEF on older firmware.
- The **Firmware Version** channel (`controller#firmwareVersion`) now appears on the Thing.
- Both channels are added to existing iQ3 Things automatically.
