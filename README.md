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

- [ksPerPixelMultiMap_emissive](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/ksPerPixelMultiMap_emissive.md): alternative to “ksPerPixelMultiMap” with extra txEmissive map working as colored mask for emissiveness.
- [ksPerPixelMultiMap_NMDetail_emissive](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/ksPerPixelMultiMap_NMDetail_emissive.md): alternative to “ksPerPixelMultiMap_NMDetail” with extra txEmissive map working as colored mask for emissiveness.
- [ksMultilayer_fresnel_nm4](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders/blob/master/docs/ksMultilayer_fresnel_nm4.md): alternative to “ksMultilayer_fresnel” with four normal maps aligned with detail maps instead of one texture mapped to main UV. Has four separate options for fixed tiling, instead of ksEmissive trick.
- stPerPixelMultiMap_specular: more advanced version of “ksPerPixelMultiMap” made by Stereo, with separate txSpecular texture for the color of specular, specular ambient, optionally colored reflections and better behaving txMaps allowing for wider variery of effects. Also, you can keep ambient occlusion in txMaps’ alpha channel instead.
- stPerPixelMultiMap_specular_damage_dirt: same as previous shader, but with damages, for car paint.

## Compilation

You can find source code for all the shaders [here](https://gitlab.com/ac-custom-shaders-patch/public/acc-shaders). Repo has a build script for Visual Code written with Node.js, which also rebuilds those packages (make sure to uncomment “Skip: basic” in “params.txt” before building). 

## Distribution

If you’re working on a mod, please feel free to include compiled shaders in published build. All those shaders are included in CSP, so if your project doesn’t target vanilla AC, doesn’t worry about it.
