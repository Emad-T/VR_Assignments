---
uid: xr-core-utils-changelog
---
# Changelog
All notable changes to this package will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [2.0.0-pre.5] - 2021-11-16

### Changed

- Property names so that they adhere to PascalCase.

### Added
- Added `XROrigin` menu item to SceneInspector that creates and configures a basic `XROrigin` in the scene.

### Fixed

- Serialization issue where upgrading to [XROrigin](xref:Unity.XR.CoreUtils.XROrigin) from [XRRig](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@1.0/api/UnityEngine.XR.Interaction.Toolkit.XRRig.html) may cause references to be broken in the component.
- Issue where [XROrigin.CameraInOriginSpacePos](xref:Unity.XR.CoreUtils.XROrigin.CameraInOriginSpacePos) was being miscalculated.
- Issue where the custom Inspector for [XROrigin](xref:Unity.XR.CoreUtils.XROrigin) was not being used.
- Warning message referencing an old property name when a Camera could not be found.
- A reflection issue with [ScriptableSettingsBase.GetInstanceByType](xref:Unity.XR.CoreUtils.ScriptableSettingsBase.GetInstanceByType(System.Type)) by renaming `EditorScriptableSettings<T>.instance` to `EditorScriptableSettings<T>.Instance`.

## [2.0.0-pre.3] - 2021-11-03

This is the first release of *XR Core Utilities* package.

### Added

- XROrigin is a new XR agnostic setup that handles session space. It will be replacing [ARSessionOrigin](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.2/api/UnityEngine.XR.ARFoundation.ARSessionOrigin.html?q=ARSessionOrigin) and [XRRig](https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@1.0/api/UnityEngine.XR.Interaction.Toolkit.XRRig.html?q=XRRig).
- All the utilities from [XR Tools Utilities](https://docs.unity3d.com/Packages/com.unity.xrtools.utils@latest?preview=1&subfolder=/manual/) (`com.unity.xrtools.utils`) package has been migrated in this package. This includes common utilities used by XR packages like MARS, AR Foundation, and Spatial Framework.

### Changed

- The minimum Unity version for this package is now 2019.4.

### Removed

- `CONTRIBUTING.md` since the package is not accepting external contribution.

### Fixed

- Company name in `LICENSE.md` file from "Unity Technologies ApS" to "Unity Technologies".
