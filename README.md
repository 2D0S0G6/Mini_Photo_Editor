# Mini Photo Editor

A lightweight, browser-based image editor that applies real-time filters and transformations using OpenCV.js, with undo/redo history and one-click export.

## Overview

Mini Photo Editor is a Next.js web application built as a course project for **20CYS212 – Multimedia Processing**. Users upload an image, apply filters and enhancements that run entirely in the browser, step backward and forward through their edit history, and download the result. All image processing happens client-side via OpenCV.js — no server-side computation is involved.

**Authors:** Aravindh P (CYS23011), Deepak SG (CYS23020)

## Features

- Image upload for common formats (PNG, JPEG, BMP) using the browser FileReader API
- Real-time filters and transformations powered by OpenCV.js:
  - Grayscale
  - Gaussian blur (low-pass)
  - Canny edge detection (high-pass)
  - Thresholding
  - Brightness adjustment
  - Rotation
- Live preview rendered to an HTML5 `<canvas>`
- Undo/redo with a thumbnail-based history viewer for jumping to any previous state
- Export the edited image as PNG (client-side, via canvas + Base64)

## Tech stack

- **Next.js 15** (App Router) with React 19
- **OpenCV.js** for image processing (loaded from `public/opencv.js`)
- **Tailwind CSS 4** with **DaisyUI** for styling
- **HTML5 Canvas** and the FileReader API
- ESLint (`eslint-config-next`)

## Getting started

Requires Node.js. From the project root:

```bash
npm install       # install dependencies
npm run dev       # start the dev server (http://localhost:3000)
```

Other scripts:

```bash
npm run build     # production build
npm run start     # serve the production build
npm run lint      # run ESLint
```

## Project structure

```
Mini_Photo_Editor/
├── public/
│   └── opencv.js               # OpenCV.js runtime loaded by the editor
├── src/
│   ├── app/
│   │   ├── layout.jsx          # root layout
│   │   ├── page.jsx            # main page
│   │   └── globals.css         # global styles (Tailwind)
│   └── components/
│       ├── PhotoEditor.jsx     # top-level editor, ties the modules together
│       ├── ControlPanel.jsx    # filter/transform controls
│       ├── ImageCanvas.jsx     # canvas preview + rendering
│       └── HistoryViewer.jsx   # undo/redo thumbnail history
├── next.config.mjs
├── postcss.config.mjs
└── package.json
```
