# ID7 Safe Cluster Map

An independent CarPlay/Android Auto navigation-map control app for BMW iDrive 7 / MGU.

This repository is derived from Robert Nisipeanu's open-source
[`idrive-apps`](https://github.com/robertnisipeanu/idrive-apps) project. Version
0.1.3 restricts the map to BMW's native 1088×480 central map layer so the
original instrument information remains visible.

## Status and safety

**Stationary testing only until this build has been verified on the car.**

The rejected whole-panel prototype covered BMW's original information because
the `panel` target sits above it. That option has been removed. If an earlier
test left the renderer on `panel`, version 0.1.3 asks it to return to `map` as
soon as the application connects.

## Add as an MGU Store source

In MGU Store, open **Settings → Add source**, enter:

```text
dwz365365/id7f
```

Choose **Releases**, then install the independent `dwz_fullscreen_cluster`
app. It uses the already-installed `waze-on-cluster` service without claiming
it as a same-source dependency. Do not replace the existing service. The
original `robertn_waze_cluster` application remains installed and is not
replaced. Restart the head unit if requested. Test only while parked in P.

To try it: start CarPlay navigation, open **ID7 Safe Map → Show on**, then
choose `Cluster`.

## Immediate recovery

1. Choose the first `Cluster` option to use the native central map.
2. If the menu cannot be used, disconnect CarPlay and perform a normal head-unit restart.
3. To return to the upstream build, remove `dwz_fullscreen_cluster` and restore
   `waze-on-cluster` from `robertnisipeanu/idrive-apps` if it was updated.

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

