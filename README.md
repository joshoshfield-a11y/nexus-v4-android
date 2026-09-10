# NEXUS v4 — Android

Audio-Reactive WebGPU Engine, wrapped in a native Android WebView shell.
Source: https://github.com/joshoshfield-a11y/NEXUS-v4 (React 19 + TS + Vite + WebGPU).

- Web bundle pre-built into `app/src/main/assets/www/` (vite production build).
- Mic input bridged: runtime RECORD_AUDIO -> WebView PermissionRequest -> getUserMedia.
- WebGPU requires an up-to-date Android System WebView (Chrome 113+).

## Build
GitHub Actions builds both debug and release (debug-key signed) APKs on every push.
Artifacts: `nexus-v4-debug.apk`, `nexus-v4-release.apk`.

## Install
Sideload `nexus-v4-release.apk`. Bump `versionCode` before each rebuild so updates install in place.

## Rebuilding the web bundle
npm install && npm run build, then copy dist/* into app/src/main/assets/www/.
