# Changelog

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
