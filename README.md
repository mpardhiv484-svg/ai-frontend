# VERITAS AI — Deepfake & Synthetic Media Detector (Frontend)

An ultra-modern, responsive, frontend-only web application designed for an AI-generated content detection platform. It provides forensic media inspection interfaces for **Images, Videos, Audio**, and **Multi-Modal 3-File Batches**.

---

## 🌟 Key Features

1. **Cyber-Tech Landing Page**
   - Prominent glowing AI shield / neural scanner brand mark.
   - High-impact typography and tagline: *"Detect AI-Generated Content with Confidence"*.
   - Large modern **START ANALYSING** button with smooth transitions and glowing accents.

2. **Analysis Selection Page**
   - 4 large interactive cards:
     - **Upload Image** (JPEG, PNG, WEBP, AVIF)
     - **Upload Video** (MP4, WebM, MOV)
     - **Upload Audio** (MP3, WAV, AAC, OGG)
     - **Upload 3 Files** (Multi-modal batch: exactly 1 image + 1 video + 1 audio)

3. **Rich File Upload Interface**
   - Drag-and-drop or file browser selection.
   - **Image Preview**: High-resolution image card with metadata.
   - **Video Preview**: HTML5 video player with controls.
   - **Audio Preview**: Custom audio player with interactive canvas waveform and play/pause toggle.
   - File details: Name, formatted size (KB/MB), format badge.
   - Controls: **Change File** and **Remove File**.
   - For **Upload 3 Files**: 3 dedicated slot cards with individual dropzones, status badges, and a convenient **"Load Demo 3-Pack"** button for 1-click presentation testing.

4. **Animated Neural Analysis Screen**
   - Dedicated scanning screen with a moving laser scan beam.
   - Canvas-based dynamic particle neural network visualizer with pulsing nodes.
   - Circular SVG progress meter counting from 0% to 100%.
   - Real-time simulated forensic status stream (frequency decomposition, diffusion latent inspection, temporal vector tracking, and vocoder harmonic checks).

5. **Comprehensive Forensic Results Screen**
   - **Verdict Banner**: Visual confidence card for:
     - 🔴 **Likely AI Generated** (e.g., 94.8% confidence)
     - 🟢 **Likely Human Generated** (e.g., 93.4% confidence)
     - 🟡 **Uncertain / Mixed Indicators** (e.g., 53.2% confidence)
   - **Demo Scenario Simulator**: Switch between AI, Human, and Uncertain states on demand with one click to demonstrate all UI states during evaluations!
   - **Detailed Forensic Breakdown**: Metrics for Latent Diffusion Fingerprint, Frequency Domain (FFT), Temporal Coherence, and Acoustic Phase Continuity.
   - **Multi-Modal Breakdown**: For 3-file uploads, displays an overarching cross-modal evaluation plus 3 dedicated individual forensic cards (Image, Video, Audio).
   - **Action Buttons**: "Analyse Another File", "Download Forensic Report" (exports text report file), and "Copy Summary".

6. **Global Navigation & Modals**
   - Sticky glassmorphic navbar with active indicator and "System Online" badge.
   - **About Modal**: Comprehensive guide to forensic methodologies and backend readiness.
   - Back button on every view.

---

## 🚀 How to Run

### Option 1: Direct in Browser (No Server Needed)
Simply double-click `index.html` or open it with any web browser (Chrome, Edge, Firefox, Safari).

### Option 2: Using Node.js / NPX
```bash
npx serve .
```

### Option 3: Using Python
```bash
python -m http.server 8000
```

---

## 🔌 Connecting a Real Backend (Future Integration)

The application is structured with a dedicated API service in [`js/api.js`](file:///c:/Users/new/Desktop/ai%20detector/js/api.js).

To connect a real Python / Flask / FastAPI / Node backend:
1. Open `js/api.js`.
2. Change `USE_REAL_BACKEND: true`.
3. Set `BACKEND_BASE_URL` to your server's endpoint (e.g., `http://localhost:8000/api/v1`).
4. The service will send a standard `multipart/form-data` POST request with the uploaded files.

---

## 📁 Project Structure

```
ai-detector/
├── index.html              # Main single-page application shell
├── README.md               # Project documentation & integration guide
├── css/
│   ├── main.css            # Base design system, CSS variables & cyber grid
│   ├── components.css      # Cards, dropzones, previews, results, modals
│   ├── animations.css      # Keyframes for scanning laser, pulses, and rotations
│   └── responsive.css      # Mobile, tablet, and widescreen adjustments
└── js/
    ├── app.js              # Application coordinator & state manager
    ├── router.js           # Seamless SPA view transitions & back stack
    ├── previews.js         # Media preview handlers & canvas audio waveform
    ├── scanner.js          # Canvas neural visualizer & circular progress meter
    ├── mockData.js         # Forensic profiles, metrics, and explanatory text
    └── api.js              # Mock API layer ready for future backend drop-in
```
