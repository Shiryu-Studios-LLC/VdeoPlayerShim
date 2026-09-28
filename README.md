# Shiryu.VideoPlayerShim

**Shiryu.VideoPlayerShim** is a Shiryu Studios LLC maintained and modified fork of **ArchiTech.VideoPlayerShim** by ArchiTechVR / TechAnon.

The original project is available at https://gitlab.com/techanon/videoplayershim and the original ArchiTechVR VPM listing is available at https://vpm.techanon.dev.

This fork keeps the original ISC license and copyright notice, while carrying Shiryu Studios-specific fixes and maintenance changes used by our VRChat projects. Internal `ArchiTech.VideoPlayerShim` namespaces and assembly names are intentionally retained for compatibility with existing scenes, components, prefabs, and scripts.

## What it does

This package provides editor play-mode support for both UnityVideo and AVProVideo in VRChat SDK projects, including YTDL/yt-dlp URL resolution.

## Install

Install **Shiryu.VideoPlayerShim** from the **Shiryu Studios Official Packages** VPM repository:

- Repository: https://packages.shiryu.org/official?download
- Package ID: `org.shiryu.videoplayershim`

The package declares `dev.architech.videoplayershim` as a legacy package so the Shiryu fork can replace the original package rather than being installed alongside it.

## AVPro editor support

Upon importing the package, it should prompt you to automatically import the required AVPro version. Accept the prompt to enable AVPro playback in editor play mode.

If the automatic import fails, you can install the matching AVPro Trial package manually from the RenderHeads releases page:
https://github.com/RenderHeads/UnityPlugin-AVProVideo/releases

**The AVPro Trial package is required for AVPro playback in Unity editor play mode.**

### Manual AVPro setup

- If you do not need AVPro support, the shim can be used without importing AVPro.
- If you do need AVPro support, use the same AVPro version that VRChat currently uses.
- To identify the version, run a VRChat world with an enabled AVPro player and inspect the VRChat debug log for a line beginning with `[AVProVideo] Initializing AVPro Video vX.X.X`.
- Download the matching trial package from RenderHeads and import it into Unity.
- Import or refresh Shiryu.VideoPlayerShim afterward.
- Configure your `VRCAVProVideoPlayer`, speakers, and screens as normal.
- Enter Play Mode and test a supported URL.

## Compatibility and attribution

This is **not the original upstream ArchiTech release**. It is a modified fork maintained by Shiryu Studios LLC.

Original project:
- **ArchiTech.VideoPlayerShim**
- Original author: **ArchiTechVR / TechAnon**
- Upstream source: https://gitlab.com/techanon/videoplayershim
- Original VPM listing: https://vpm.techanon.dev

Shiryu Studios maintains this fork and is responsible for the modifications distributed from this repository. The original ISC copyright and permission notice remain in `LICENSE.md`.

A portion of the code in the package is based on modified logic from the AVPro Trial package so that it works with the VRChat SDK / ClientSim. Rights in the original AVPro Trial code remain with RenderHeads.

## Support

For issues specific to the Shiryu-maintained fork, use this repository:
https://github.com/Shiryu-Studios-LLC/VdeoPlayerShim

For behavior specific to the original ArchiTech project, consult the upstream project linked above.
