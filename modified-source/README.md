# Modified files

The complete upstream source is available at:

https://github.com/robertnisipeanu/idrive-apps

This directory contains the files changed by this build:

- `robertn_waze_cluster.js`: exposes only the native cluster, HUD, both and off
  choices; the released app is repackaged under the independent
  `dwz_fullscreen_cluster` ID.
- `waze_cluster_control.js`: refuses the whole-panel presentation and returns
  an earlier `panel` test to the native `map` target when it connects.
- `waze-on-cluster.conf`: retained only as a record of the rejected prototype;
  version 0.1.3 does not install it or modify the existing renderer service.

The release packages include the corresponding upstream files and binaries.
