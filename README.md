# 🖼️ Mini Photo Editor

**Course**: 20CYS212 – Multimedia Processing  
**Team Members**:  
- Aravindh P (CYS23011)  
- Deepak SG (CYS23020)

---

## 📘 Project Overview

**Mini Photo Editor** is a lightweight, browser-based image editing tool built as a course project for Multimedia Processing. It enables users to upload images, apply a range of real-time filters and enhancements, track edit history, and export the final image—all through an interactive and modern user interface.

---

## 🧩 Modules Implemented

### 1. **User Interface (UI) Module**
- Built using **ReactJS** with **TailwindCSS** (DaisyUI).
- Includes upload button, filter controls, undo/redo, and save options.
- Responsive and clean design for a smooth user experience.

### 2. **File Management Module**
- Supports image upload in formats like `.png`, `.jpeg`, and `.bmp`.
- Uses FileReader API to load image into memory.
- Handles image preview and reload.

### 3. **Image Processing Engine**
- Core computations done using **OpenCV.js**.
- Applies pixel-level transformations with convolution and matrix operations.
- Modular design allows future extension of filters and operations.

### 4. **Filters & Effects Module**
Includes multiple filters such as:
- Grayscale  
- Gaussian Blur (low-pass)  
- Canny Edge Detection (high-pass)  
- Thresholding  
- Brightness Adjustment  
- Rotation  

Each filter is applied on the fly and rendered instantly.

### 5. **Image Preview Module**
- Real-time display of the currently processed image via `<canvas>`.
- Automatically updates after each applied transformation.

### 6. **Export Module**
- Enables downloading the edited image in `.png` format.
- Uses Canvas API and Base64 conversion to allow client-side saving.

### 7. **Undo/Redo Module**
- Maintains image history using stack logic.
- Lets users move backward and forward between editing states.
- Includes a thumbnail-based history viewer for direct state selection.

---

## 🧪 Technologies Used

- **ReactJS**  
- **OpenCV.js**  
- **TailwindCSS (DaisyUI)**  
- **HTML5 Canvas**  
- **JavaScript (ES6+)**

---

## 🎯 Key Learnings

- Implementing modular architecture for real-time image processing.
- Applying advanced filters using OpenCV.js.
- Using React state management for undo/redo history.
- Designing a responsive UI with TailwindCSS.
- Understanding low-level concepts like kernels, edge detection, padding, and filtering.

---
