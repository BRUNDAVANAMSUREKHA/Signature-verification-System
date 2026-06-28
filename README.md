<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=DM+Sans&size=32&duration=3000&pause=1000&color=6366F1&center=true&vCenter=true&width=700&lines=Signature+Verification+System+✍️;AI-Powered+Signature+Verification;Webcam+Capture+%2B+SSIM+Comparison;Built+with+Python+%2B+OpenCV" alt="Typing SVG" />

<br/>

# ✍️ Signature Verification System
### *Accurate Signature Verification Using Structural Similarity Index*

<br/>

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Tkinter](https://img.shields.io/badge/Tkinter-GUI-10B981?style=for-the-badge&logo=python&logoColor=white)](https://docs.python.org/3/library/tkinter.html)
[![OpenCV](https://img.shields.io/badge/OpenCV-Image_Processing-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org/)
[![scikit-image](https://img.shields.io/badge/scikit--image-SSIM-FF6B6B?style=for-the-badge)](https://scikit-image.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Array_Processing-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)](LICENSE)


</div>

---

## 📌 Overview

**Signature Verification System** is a Python desktop application that verifies whether two signatures belong to the same person. It uses **OpenCV** for webcam-based signature capture and **SSIM (Structural Similarity Index)** from scikit-image to compute how similar two signature images are — giving a precise similarity percentage and a clear match or no-match result.

> 🔍 *If the similarity score exceeds **85%**, the signatures are confirmed as a match. Below 85%, they are flagged as different.*

---

## 🖥️ App Flow

```
Launch App
     ↓
Load Signature 1              Load Signature 2
┌─────────────┐              ┌─────────────┐
│ 📷 Capture  │              │ 📷 Capture  │
│   (Webcam)  │      OR      │   (Webcam)  │
│ 📂 Browse   │              │ 📂 Browse   │
│   (File)    │              │   (File)    │
└─────────────┘              └─────────────┘
        ↓                          ↓
   Image saved                Image saved
   to ./temp                  to ./temp
                  ↓
           Click Compare
                  ↓
        SSIM Algorithm runs
                  ↓
     ┌──────────────────────────┐
     │  Score ≥ 85%  →  ✅     │
     │  Signatures Match!       │
     ├──────────────────────────┤
     │  Score < 85%  →  ❌     │
     │  Signatures Don't Match! │
     └──────────────────────────┘
```

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 📷 Signature Input
- **Webcam Capture** — live capture via `Capture` button
- **File Browse** — load any image from your system
- Supports both methods for each signature slot
- Images saved temporarily in `./temp` folder

</td>
<td width="50%">

### 🔬 Comparison Engine
- **SSIM Algorithm** — Structural Similarity Index
- Returns exact **similarity percentage**
- **85% threshold** for match/no-match decision
- Handles grayscale conversion automatically

</td>
</tr>
<tr>
<td width="50%">

### 🖥️ Desktop GUI
- Built with Python **Tkinter**
- Clean, intuitive interface
- Real-time feedback via popup messages
- No browser or internet needed

</td>
<td width="50%">

### 📊 Result Feedback
- ✅ **Match** — similarity ≥ 85%
- ❌ **No Match** — similarity < 85%
- Displays exact similarity score
- Instant result popup

</td>
</tr>
</table>

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python 3.x** | Core programming language |
| **Tkinter** | Desktop GUI — buttons, windows, layout |
| **OpenCV** (`cv2`) | Webcam access and image preprocessing |
| **scikit-image** | SSIM algorithm for similarity comparison |
| **NumPy** | Image array manipulation |

---

## 📁 Project Structure

```
Signature-Verification-System/
│
├── main.py              # Main application entry point
├── signature.py         # Signature capture and SSIM comparison logic
└── README.md            # Project documentation
```

---

## ⚙️ Installation & Setup

### Prerequisites

| Tool | Download |
|---|---|
| Python 3.x | https://www.python.org/downloads/ |
| Webcam | Required for capture feature |
| Git | https://git-scm.com/ |

---

### Step 1 — Clone the Repository

```bash
git clone https://github.com/BRUNDAVANAMSUREKHA/Signature-Verification-System.git
cd Signature-Verification-System
```

---

### Step 2 — Create Virtual Environment

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Mac / Linux
source venv/bin/activate
```

---

### Step 3 — Install Dependencies

```bash
pip install opencv-python-headless
pip install numpy
pip install scikit-image
```

Or all at once:

```bash
pip install -r requirements.txt
```

---

### Step 4 — Run the Application

```bash
python main.py
```

---

## 🖥️ Usage Guide

### Method 1 — Webcam Capture
1. Launch the app with `python main.py`
2. Click **Capture** for Signature 1 — webcam opens, capture the signature
3. Click **Capture** for Signature 2 — repeat for the second signature
4. Click **Compare** — result appears instantly

### Method 2 — Browse Existing Images
1. Launch the app with `python main.py`
2. Click **Browse** for Signature 1 — select an image file from your system
3. Click **Browse** for Signature 2 — select the second image file
4. Click **Compare** — similarity score and result displayed

### Method 3 — Mix Both
- Use **Capture** for one signature and **Browse** for the other
- Click **Compare** — works with any combination

---

## 🔬 How SSIM Works

**SSIM (Structural Similarity Index)** compares two images based on three factors:

| Factor | What It Measures |
|---|---|
| **Luminance** | Overall brightness similarity |
| **Contrast** | Difference in image contrast |
| **Structure** | Patterns and edges in the image |

```
SSIM Score = 1.0   →  Images are identical
SSIM Score = 0.85  →  Threshold (Match confirmed ✅)
SSIM Score < 0.85  →  Signatures are different ❌
SSIM Score = 0.0   →  Images are completely different
```

> Both images are converted to **grayscale** and resized to the same dimensions before comparison to ensure accurate results.

---

## 🔭 Roadmap

```
v1.0  ✅  Webcam capture for signatures
v1.1  ✅  File browse for signature images
v1.2  ✅  SSIM-based similarity comparison
v1.3  ✅  85% threshold match/no-match result
v2.0  🚧  Adjustable similarity threshold slider
v2.1  📅  Save and store signature database
v2.2  📅  One-to-many signature verification
v2.3  📅  Export comparison report as PDF
v3.0  📅  Deep learning-based verification model
```

---

## 👩‍💻 Author

<div align="center">

**Surekha Brundavanam**

[![GitHub](https://img.shields.io/badge/GitHub-BRUNDAVANAMSUREKHA-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/BRUNDAVANAMSUREKHA)

</div>

---

## 📄 License

> ⚠️ **Proprietary License** — All rights reserved © 2025 **Surekha Brundavanam**
>
> This project and its source code may **not** be used, copied, modified, merged, published, distributed, sublicensed, or sold without explicit written permission from the author.
>
> Unauthorized use, reproduction, or distribution of this software, via any medium, is strictly prohibited.
>
> For permissions, contact: [@BRUNDAVANAMSUREKHA](https://github.com/BRUNDAVANAMSUREKHA) on GitHub

---

<div align="center">

**✍️ Signature Verification System — Verify Signatures with Precision**

*If this project helped you, consider giving it a ⭐ on GitHub!*

</div>
