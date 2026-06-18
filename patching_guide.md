# Atmosphere-HATS Patching Guide

This repository is a fork intended for local Atmosphere customization. Changes documented here are fork-local patches and are not intended to be proposed upstream unless explicitly noted.

## Firmware Version eMMC Label

Atmosphere displays its version in System Settings through `set_mitm` by modifying the firmware `display_version` string.

Upstream format:

```text
#.#.#|AMS #.#.#|S
#.#.#|AMS #.#.#|E
```

Atmosphere-HATS format:

```text
#.#.#|AMS #.#.#|SYS
#.#.#|AMS #.#.#|EMU
```

Patch location:

```text
stratosphere/ams_mitm/source/set_mitm/setsys_mitm_service.cpp
```

Relevant code:

```cpp
const char *emummc_str = emummc::IsActive() ? "EMU" : "SYS";

util::SNPrintf(display_version, sizeof(display_version), "%s|AMS %u.%u.%u|%s", g_ams_firmware_version.display_version, api_info.GetMajorVersion(), api_info.GetMinorVersion(), api_info.GetMicroVersion(), emummc_str);
```

Keep the label short. The destination field is fixed-size, and the surrounding code assumes the final display string fits without truncation.
