## Hi, i'm Nicolas de Haan 👋

👀 I am a student a Code University of applied science in Berlin, transitioning from a background in business management. I’m now channeling my problem-solving and analytical skills into web development.
I'm passionate about building real-time, interactive web applications using Next.js, Convex, TypeScript, and Three.js. I began my programming journey by learning the fundamentals of C, which grounded me in low-level logic and performance. Over time, my curiosity led me to explore 3D web development, and I'm now focused on innovating in that space through projects like TravelFlow or a 3D visualisation book. 

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
yarn install

# run the project
yarn run dev

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

## 🌌 Changing the Background

Want a different vibe than the default studio? You can easily swap out the background or even add your own 3D environment.

# 🔁 Option 1: Use a Different Preset

Inside Experience.jsx, you'll find this line:

```
<Environment preset="studio" />
```
Change the "studio" preset to any of these available options:

* "sunset"

* "dawn"

* "night"

* "warehouse"

* "forest"

* "apartment"

* "city"

* "park"

For example:
```
<Environment preset="sunset" />
```
📸 Instantly gives your book a warm evening glow!

# 🌍 Option 2: Use a Custom HDRI

1. Get a .hdr environment map from websites like polyhaven.com

2. Place the file in your /public directory.

3. Import and use it like this:

```
<Environment files="/your-hdri.hdr" background />

```
This sets your image as the full 3D background and lighting source. Make sure it’s a .hdr file for the best results.

## 🧙‍♂️ Future Ideas

* Incorporate hover tooltips with photo metadata

* Drag-to-flip page gestures

* Mobile support + gyroscope interaction

## 🚀 Deployment

The 3D Book Visualization project is deployed on Vercel, offering a seamless and responsive user experience directly in the browser. You can access the live version of the app below:

[Live Demo: 3D Book Visualization](https://3-dbookvisu-b3m3xt7ww-nicolas-projects-93e9a5a9.vercel.app/)

# 🔧 Deployment Details:

Hosting: Vercel

Frontend: Built with React and Three.js for interactive 3D rendering.

CI/CD: Automatically deployed on Vercel via GitHub with every push to the main branch.

## 📚 Credits & Inspirations

* react-three-fiber : https://github.com/pmndrs/react-three-fiber

* drei : https://github.com/pmndrs/drei

* maath : https://github.com/pmndrs/maath

* Your memories 📸
