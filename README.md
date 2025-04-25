## 📖✨ 3Dbookvisu
    
    "Because flipping through memories should feel like magic."

3Dbookvisu is an immersive 3D photo book built with React, Three.js, and Vite — blending interactivity, animation, and nostalgia into one virtual experience.

## 🚀 Features

🌀 Page Curling Animation: Each page bends and flows using skinned meshes and bone-based animation (no shortcuts taken).

🌄 Photo Textures: Every page is covered in beautiful textures from your photo collection.

🎧 Audio Feedback: Pages flip with a satisfying sound for that extra "real-book" feel.

💡 Lighting & Shadows: Studio-style lighting setup with soft shadows for cinematic vibes.

🧭 Orbit Controls: Rotate, zoom, explore the book from all angles.

🧠 State with Jotai: Lightweight state management to keep track of your flipping journey.

## 🧱 Built With

React + Vite – Lightning-fast dev experience with HMR.

@react-three/fiber – React wrapper for Three.js.

@react-three/drei – Useful helpers like Float, Environment, and useCursor.

Jotai – Atom-based state management.

Three.js – Core of the visual magic.

Maath – For beautiful easing and animations.

## 🛠️ Project Structure

```
📁 src/
├── Book.jsx        // Core of the 3D book logic, materials, bones & animations
├── Experience.jsx  // Scene setup: lighting, controls, floating
├── UI.jsx          // Interactive UI with page buttons and sound effects
├── assets/
│   └── textures/   // Your image textures
│   └── audios/     // Page flip sound
```

## 🧪 Dev Setup

```
# clone the project
git clone https://github.com/aimetamere/3Dbookvisu.git
cd 3Dbookvisu

# install dependencies
npm install

# run the project
npm run dev

```
Now open your browser at http://localhost:5173 and enjoy the magic ✨

## 🔍 Behind the Scenes

# The PageAnatomy:

* Each page is a SkinnedMesh with multiple bones controlling segments of the mesh.

* Curvature is controlled by different easing and rotation functions:

* insideCurveStrength, outsideCurveStrength, turningCurveStrength

* Cover and back pages have a special roughness map for realistic material finish.

# Textures are preloaded to avoid runtime lags:

```
useTexture.preload(`/textures/${page.front}.jpg`);
```

## 🌈 Add Your Own Pages

Update your UI.jsx:
```
const pictures = [
  "your-image-1",
  "your-image-2",
  ...
];
```
Add your .jpg images to /public/textures/ and you're done!

## 🧙‍♂️ Future Ideas

* Incorporate hover tooltips with photo metadata

* Drag-to-flip page gestures

* Mobile support + gyroscope interaction

## 🧑‍🎨 Gallery


## 📚 Credits & Inspirations

* react-three-fiber : https://github.com/pmndrs/react-three-fiber

* drei : https://github.com/pmndrs/drei

* maath : https://github.com/pmndrs/maath

* Your memories 📸