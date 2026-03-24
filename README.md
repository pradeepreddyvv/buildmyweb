# BuildMyWeb — Hand-Drawn Wireframe to HTML/CSS

**Capstone Project, PES University**

End-to-end platform that converts hand-drawn wireframes into production HTML/CSS using a custom **CNN+CTC deep learning model** and **OpenCV** computer vision pipeline, achieving **95% text recognition accuracy**. Includes a React-based live editor for real-time UI customization, reducing prototyping time by **30%**.

[![Demo](https://img.shields.io/badge/YouTube-Demo-red)](https://www.youtube.com/watch?v=yyLzYmfoxHw)
[![License](https://img.shields.io/badge/License-MIT-green)](MIT_License)

## How It Works

```
Hand-drawn wireframe (photo/scan)
        │
        ▼
┌───────────────────┐
│  OpenCV Pipeline   │  → Edge detection, contour analysis,
│  (Segmentation)    │    component identification
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  CNN + CTC Model   │  → Text recognition from UI elements
│  (TensorFlow)      │    95% accuracy on handwritten text
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  HTML/CSS Generator│  → Structured layout generation
│  (Flask Backend)   │    from detected components
└────────┬──────────┘
         │
         ▼
┌───────────────────┐
│  React Live Editor │  → Real-time preview and editing
│  (Client)          │    Download final HTML file
└───────────────────┘
```

## Tech Stack

| Layer | Technologies |
|-------|-------------|
| CV/ML | OpenCV (segmentation), TensorFlow (CNN+CTC model) |
| Backend | Python, Flask |
| Frontend | React, Node.js |
| Model | Pre-trained CNN+CTC (`model_20.h5`) for handwritten text recognition |

## Examples

### Input (Hand-drawn wireframe)
<img src="/test.jpeg" height="400" width="300" />

### Output (Generated HTML)
<img src="/output.png" />

More examples in [`/input`](input/) and [`/output`](output/) directories.

## Setup

**Terminal 1 — Frontend:**
```bash
cd client
npm install
npm run build
npm start
```

**Terminal 2 — Backend:**
```bash
pip install -r requirements.txt
python3 server.py
```

## Demo

[![BuildMyWeb Demo](https://img.youtube.com/vi/yyLzYmfoxHw/maxresdefault.jpg)](https://www.youtube.com/watch?v=yyLzYmfoxHw)

## Project Structure

```
├── client/             # React frontend with live HTML editor
├── segmentation/       # OpenCV image processing pipeline
├── server.py           # Flask backend — CV pipeline + HTML generation
├── model_20.h5         # Pre-trained CNN+CTC model
├── input/              # Sample hand-drawn wireframes
├── output/             # Generated HTML outputs
├── flowchart.png       # System architecture diagram
└── requirements.txt    # Python dependencies
```

## License

[MIT License](MIT_License)

## Author

**Pradeep Reddy Venuthurla**, PES University — B.Tech Computer Science & Engineering
