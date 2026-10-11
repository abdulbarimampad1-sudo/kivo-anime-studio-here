# Kivo Anime Studio

Kivo Anime Studio is a local-first desktop workspace for building anime scenes, animating characters, editing audio and exporting video.

## Current implementation

The React + TypeScript interface is served with Vite. The Rotoscope workspace previews a user-selected video directly in the browser. The selected file is not uploaded or persisted by the static site. Other studio areas and the rotoscope AI pipeline remain placeholders.

## Run locally

```sh
npm install
npm run dev
```

## Planned architecture

- `src/`: editor UI and client state
- `src-tauri/`: desktop shell (future increment)
- `engine/`: local Python video service and future vision/media pipelines
- `shared/`: request and project schemas
- `models/`: documentation for user-managed local model files
- `projects/`: local project data (kept out of source control when populated)

The frontend can be deployed as a static site. It does not require Python, FFmpeg, FFprobe, or a hosted AI service just to open and preview a video. A selected file remains available only in the current browser session.
