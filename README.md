# URP Alpha Masked

A fork of URP 17.4.0 that enables alpha-to-coverage in the SpeedTree 7 billboard forward pass, matching the existing SpeedTree 7 and SpeedTree 8 forward passes. With MSAA enabled, this allows smoother alpha-clipped billboard edges.

Standard URP shaders and Shader Graph targets retain their upstream behavior: alpha-to-coverage is enabled automatically for opaque, alpha-clipped materials when MSAA is available. Shadow, depth, and deferred passes are unchanged.

## Migrating from earlier versions of this fork

The custom `Unlit Alpha To Coverage` Shader Graph target has been removed. Before upgrading, switch graphs using it to the standard `Unlit` target. For alpha-to-coverage, use an opaque surface with Alpha Clipping and enable MSAA in URP.
