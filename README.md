# ID7 Full-screen Cluster Map (experimental)

Experimental full-screen CarPlay/Android Auto navigation-map mode for BMW iDrive 7 / MGU.

This repository is derived from Robert Nisipeanu's open-source
[`idrive-apps`](https://github.com/robertnisipeanu/idrive-apps) project. It adds
an HMI choice named `Cluster — FULL (experimental)` and configures the map
renderer to stretch the phone's 1088×480 cluster stream to the 1920×720 panel.

## Status and safety

**Stationary testing only. Do not drive with the experimental full-screen mode enabled.**

The iDrive 7 `panel` target is rendered above the stock gauges. The current
prototype can therefore cover speed, battery, gear, ACC, media cards and vehicle
warnings. The preview image is a design target, not a real-car result. The
software has passed host-side JavaScript tests but has not been validated on a
real BMW instrument cluster.

The normal central-map mode remains available. Full-screen selection is not
saved across a head-unit restart, so a normal restart returns to the safer
central-map target.

## Add as an MGU Store source

In MGU Store, open **Settings → Add source**, enter:

```text
dwz365365/id7f
```

Choose **Releases**, install/update `waze-on-cluster` first, then
`robertn_waze_cluster`. Restart the head unit if requested. Test only while
parked in P.

To try it: start CarPlay navigation, open **Waze on cluster → Show on**, then
choose the final option, `Cluster — FULL (experimental)`.

## Immediate recovery

1. Choose the first `Cluster` option to return to the native central map.
2. If the menu cannot be used, disconnect CarPlay and perform a normal head-unit restart.
3. To return to the upstream build, remove these two experimental components
   in MGU Store and reinstall the official versions from
   `robertnisipeanu/idrive-apps`.

## Contents

- `modified-source/` — modified app sources and renderer configuration.
- `install/` — offline USB ZIP and the two packages used by the release.
- `preview.png` — visual target mockup only.

## Testing

- `test_control.js`: 53/53 passed.
- `test_page.js`: passed.
- `test_profiles.js`: 21/21 passed.
- `test_i18n.js`: 32 locales, 11,614 checks passed.
- Real vehicle: **not tested**.

## License and attribution

GPL-3.0-or-later. Copyright remains with the original contributors for upstream
code. See `LICENSE` and the upstream repository for full history and notices.

