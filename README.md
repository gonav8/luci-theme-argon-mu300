# Argon MU300 Theme for OpenWrt 25.12.x

A MU300-focused Argon theme variant. It retains Argon's familiar layout and color language while giving the MU300 cellular app's dashboard, signal cards, traffic summaries, and controls matching Argon surfaces in light and dark modes.

Install a compatible MU300 LuCI app separately to provide the **Status dashboard** and **Cellular** menus plus live modem and system data. This theme styles those existing pages; it does not duplicate the app's device-specific functionality. See [MU300.md](MU300.md).

## Features

- Argon-style light and dark styling for the MU300 status dashboard and cellular controls.
- OpenWrt 25.12 APKv3 package built and attached to GitHub Releases by the included Actions workflow.
- No separate Argon configuration app is required for the MU300 theme styling.

## Installation (OpenWrt 25.12.x)

Use the latest release tag and APK filename shown on the [Releases page](https://github.com/gonav8/luci-theme-argon-mu300/releases). For version `2.5.0-r1`, install with:

```sh
apk update
uclient-fetch -O luci-theme-argon-2.5.0-r1.apk https://github.com/gonav8/luci-theme-argon-mu300/releases/download/v2.5.0-r1/luci-theme-argon-2.5.0-r1.apk
apk add --allow-untrusted --force-reinstall ./luci-theme-argon-2.5.0-r1.apk
```

Install a compatible `luci-app-mu300` package separately, following the [MU300 project's instructions](https://github.com/kanoqwq/mu300-linux). The theme package provides the appearance only; the MU300 app provides the dashboard, Cellular menu, and live modem data.

## Build and release

Push a version tag such as `v2.5.0-r1` to run the GitHub Actions build. The workflow uses the official OpenWrt 25.12.2 x86/64 SDK to produce the architecture-independent LuCI theme APK and publishes the APK plus a SHA-256 checksum as release assets. You can also run the workflow manually from the Actions tab and select an OpenWrt 25.12.x SDK version.

Package version: `2.5.0-r1`.
