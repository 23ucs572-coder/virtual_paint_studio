# 🎨 Virtual Paint v2  
### Real-Time Hand-Gesture Drawing App (React + Vite + MediaPipe)

Virtual Paint v2 is an advanced hand-gesture-based drawing application that allows users to draw on a digital canvas using only their **index finger** detected through a webcam.  
Built using **React**, **Vite**, **MediaPipe Hands**, and **HTML5 Canvas**, the app showcases real-time hand tracking, gesture control, and smooth drawing — all directly in the browser.

---

## 🌟 Features

### 🖐 Hand Tracking
- Real-time detection using MediaPipe Hands  
- Tracks 21 hand landmarks  
- High-accuracy fingertip detection (landmark 8)

### ✏️ Drawing Engine
- Draw using your index finger tip  
- Smooth and continuous rendering  
- Zero-touch drawing experience

### 🎨 Customization Tools
- Brush size control (5 px – 50 px)  
- Full color picker for brush color  
- Clear canvas with one click  

### 👁 Visualization Options
- Toggle hand landmark overlay  
- Shows skeleton lines + fingertip markers  
- Helpful for debugging gestures  

### ⚙️ Controls
- Start Camera  
- Stop Camera  
- Clear Canvas  
- Change Brush Size  
- Pick Brush Color  

### 📱 Responsive UI
- Works on laptop and desktop screens  
- Optimized for realtime video + canvas rendering  

---

## 🧠 How It Works

### 1. Webcam Access  
The app uses the browser’s `MediaDevices.getUserMedia()` API to access the webcam and stream video on a `<video>` element.

### 2. Hand Detection  
MediaPipe Hands analyzes each frame and detects:
- Hand presence  
- 21 landmark coordinates  
- Index finger position  

### 3. Finger Tracking  
The app reads:
- Landmark **8** = Index finger tip  
- Converts normalized (0–1) coordinates → canvas coordinates  

### 4. Drawing Engine  
Every animation frame:
- If drawing mode is active → draw a line  
- Uses previous and current fingertip position  
- Applies selected color + brush size  

### 5. Overlay Rendering  
Two separate layers:
- Canvas for drawing  
- Canvas for hand landmark overlays (optional)

This separation keeps drawings clean and tracking visuals clear.

---

## 📁 Project Structure

virtual_paint_v2/
│── public/
│── src/
│ ├── components/
│ ├── hooks/
│ ├── styles/
│ ├── App.jsx
│ ├── main.jsx
│── package.json
│── vite.config.js
│── README.md


---

## 🛠 Tech Stack

- **React 18**  
- **Vite** (fast dev server & bundler)  
- **MediaPipe Hands**  
- **HTML5 Canvas API**  
- **JavaScript (ES6+)**  
- **CSS / Tailwind (optional)**  

---

## 📦 Prerequisites

Before running the project, ensure you have:

- **Node.js 16+**  
- **npm or yarn**  
- **A webcam**  

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/23ucs572-coder/virtual_paint_studio.git


