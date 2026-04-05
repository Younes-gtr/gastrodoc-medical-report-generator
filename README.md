# 🏥 GastroDoc – Medical Report Generation Tool

**GastroDoc** is a lightweight Windows application designed to automate the integration of medical images into PDF reports for a gastroenterology clinic.

> ⚠️ Due to confidentiality constraints, the source code is not publicly available.

---

## 📌 Overview

This project was developed for a gastroenterology clinic in Montreux, Switzerland.

The clinic faced a recurring issue:  
adding medical images (e.g. scans) into reports manually using Word was **time-consuming, inconsistent, and error-prone**.

**GastroDoc solves this by:**
- Automating image insertion into PDF reports
- Ensuring consistent layout and scaling
- Producing clean, professional documents in seconds

---

## 🎯 Key Features

- 📄 Load existing medical PDF reports  
- 🖼️ Insert multiple images automatically  
- 📐 Smart scaling (no distortion)  
- 🧩 Dynamic layout based on image count (1–6 images)  
- 📦 Automatic PDF compression  
- 🖥️ Simple and intuitive graphical interface  

---

## 🎥 Demo

![Demo](docs/demo_gastrodoc.gif)

For the full demo video, click here: [Watch full demo](https://drive.google.com/file/d/1UZYDRAwrm-1drUV841dFysvmKA_jvDAg/view)

---

## 🛠️ Tech Stack

- **Language:** C  
- **GUI:** GTK  
- **PDF Processing:** Poppler  
- **Rendering:** Cairo  
- **Compression:** Ghostscript  
- **Build/Packaging:** MinGW (Windows)

---

## 🧠 Architecture Overview

The application follows a simple and efficient pipeline:

1. Load PDF using Poppler  
2. Extract text layout to detect content boundaries  
3. Compute available space dynamically  
4. Insert and render images with Cairo  
5. Compress final document using Ghostscript  

---

## ⚙️ Key Technical Challenges

### 1. Detecting the End of Text in PDFs

**Problem:**  
Images needed to be inserted *after* the report text without overlap or excessive spacing.

**Solution:**  
Used Poppler’s text extraction to locate the last line of text and dynamically determine where image insertion should begin.

---

### 2. Dynamic Image Layout

**Problem:**  
The layout had to adapt depending on the number of images while staying readable and visually balanced.

**Solution:**  
Implemented layout rules for different scenarios (1 to 6 images), calculating:
- Positioning  
- Spacing  
- Scaling  

This ensured consistent and professional output across all cases.

---

## 🚀 Result

- Successfully deployed in a real clinical environment  
- Significantly reduced time spent on report formatting  
- Improved consistency and visual quality of medical reports  
- Simplified workflow for non-technical staff  

---

## 🔒 Disclaimer

This software was developed for a real medical clinic.  
For privacy and confidentiality reasons, the full source code is not publicly available.

A demonstration or technical discussion can be provided upon request.

---

## 📬 Contact

If you'd like to know more about this project or discuss similar work, feel free to reach out.
