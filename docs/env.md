## Environment variables

Unless specified otherwise, a variable is enabled if and only if it's set to `1`

### DRM

`AQ_DRM_DEVICES` -> Set an explicit list of DRM devices (GPUs) to use. It's a semicolon-separated list of paths, with the first being the primary. E.g. `/dev/dri/card1;/dev/dri/card0`
`AQ_NO_ATOMIC` -> Disables drm atomic modesetting
`AQ_MGPU_NO_EXPLICIT` -> Disables explicit syncing on mgpu buffers
`AQ_NO_MODIFIERS` -> Disables modifiers for DRM buffers
`AQ_NO_BLIT` -> Disables multi-GPU blitting, forces direct import (for testing cross-GPU direct scanout)
`AQ_SECONDARY_NO_RENDERER` -> Skips EGL renderer creation on secondary GPUs. Useful when the secondary GPU is dedicated to client rendering (e.g., game) and shouldn't have compositor contexts stealing resources

### Debugging

`AQ_TRACE` -> Enables trace (very verbose) logging
