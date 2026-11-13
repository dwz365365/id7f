# Modified files

The complete upstream source is available at:

https://github.com/robertnisipeanu/idrive-apps

This directory contains the files changed by this prototype:

- `robertn_waze_cluster.js`: adds the full-screen choice to the HMI list; the
  released app is repackaged under the independent `dwz_fullscreen_cluster` ID.
- `waze_cluster_control.js`: switches between `map` and `panel` targets and
  deliberately does not persist the experimental full-screen choice.
- `waze-on-cluster.conf`: uses `map_rect = 0,0,1920,720`; this is rejected on
  the normal 1088×480 target and accepted on the 1920×720 panel target.

The release packages include the corresponding upstream files and binaries.
