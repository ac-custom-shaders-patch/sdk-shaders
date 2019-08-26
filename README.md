# New shaders for AC

[![Source: https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders](https://img.shields.io/badge/source-CSP%20shaders-brightgreen.svg)](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders) 
[![Documentation: https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/tree/master/docs](https://img.shields.io/badge/documentation-more%20info-brightgreen.svg)](https://github.com/ac-custom-shaders-patch/sdk-shadershttps://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/tree/master/docs) 
[![Download: /releases/latest](https://img.shields.io/badge/download-latest%20version-brightgreen.svg)](https://github.com/ac-custom-shaders-patch/sdk-shaders/releases/latest) 

New shaders for AC, compiled for original AC and for SDK (ksEditor). If you’re using CM or JSGME, easiest way to get them working is to [download latest pack](https://github.com/ac-custom-shaders-patch/sdk-shaders/releases/latest) from versions section.

## Older SDK

If you’re using old ksEditor (before AC’s 1.2.2 update, with white background) and it’s not in “assettocorsa/sdk/editor” folder, you would need to install shaders manually.

## Files

- `ac-new.zip`: new shaders for vanilla AC;
- `sdk-new.zip`: new shaders for AC SDK (ksEditor) for versions greater than 1.2.2 (with grey/colored background);
- `sdk-old.zip`: new shaders for AC SDK for versions before 1.2.2 (with white background).

## Shaders

- [ksPerPixelMultiMap_emissive](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/ksPerPixelMultiMap_emissive.md): alternative to “ksPerPixelMultiMap” with extra txEmissive map working as colored mask for emissiveness; 
- [ksPerPixelMultiMap_NMDetail_emissive](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/ksPerPixelMultiMap_NMDetail_emissive.md): alternative to “ksPerPixelMultiMap_NMDetail” with extra txEmissive map working as colored mask for emissiveness;
- [smDigitalScreen](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/smDigitalScreen.md)¹: shader for digital screens emulating either TNT or IPS matrix;
- [smWaterSurface](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/smWaterSurface.md)¹: shader for animated water surface of specified type.

> ¹ *If you only target CSP, or could use some fallback shader for vanilla AC, please consider using extension config with “material_….ini” thing instead. In general, it’s easier to set, and, for example, if in future some improved “smWaterSurface2” would appear, those material configs would be able to switch to it without any compatibility issues by readjusting the way parameters are applied in material template (without any need to update actual car or track config).*

## Compilation

You can find source code for all the shaders [here](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders). Repo has a build script for Visual Code written with Node.js, which also rebuilds those packages (make sure to uncomment “Skip: basic” in “params.txt” before building). 

## Distribution

If you’re working on a mod, please feel free to include compiled shaders in published build. All those shaders are included in CSP, so if your project doesn’t target vanilla AC, doesn’t worry about it.