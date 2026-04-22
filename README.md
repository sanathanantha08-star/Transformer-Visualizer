

# 🚀 Transformer Explainer (Interactive Visualizer)

An interactive, browser-based visualization tool to **understand how Transformer models (like GPT-2)** process text step-by-step — from tokenization to output probabilities.

---

## 🧠 What This Project Does

This project visually breaks down the **Transformer architecture** into intuitive, animated components:

* 🔤 Tokenization
* 🔢 Embeddings (vector representations)
* 🔍 Multi-Head Self-Attention (with attention maps + Q/K/V)
* 🧱 Transformer Blocks (12 layers)
* 🔁 Residual Connections
* ⚙️ MLP (Feedforward layers)
* 📊 Output probability distribution (next-token prediction)

All computations are **precomputed and hardcoded** for educational clarity — no backend or ML inference required.

---

## 🎯 Key Features

### ✨ Interactive Controls

* **Temperature slider** → controls randomness of output
* **Top-k / Top-p sampling**
* Switch between **example inputs**
* Navigate across **attention heads** and **transformer blocks**

### 🔬 Deep Visualization

* Attention heatmaps (token-to-token relationships)
* Q / K / V vector views
* MLP expansion & compression phases
* Animated data flow across layers

### 🎨 Rich UI

* Fully custom UI (no frameworks)
* Smooth animations + transitions
* Responsive layout with scrollable pipeline

---

## 🏗️ Architecture Overview

This visualizer mimics a **GPT-2 Small** model:

* 12 Transformer Blocks
* 12 Attention Heads per block
* 768-dimensional embeddings
* 50,257 token vocabulary

Pipeline:

```
Input Text
   ↓
Tokenization
   ↓
Embeddings + Positional Encoding
   ↓
[ Transformer Block × 12 ]
   ├── Multi-Head Attention
   ├── Residual Connection
   ├── MLP (Feedforward)
   └── Residual Connection
   ↓
Final Linear Layer
   ↓
Softmax → Output Probabilities
```

---

## 📂 Project Structure

```
.
├── index.html     # Main app (HTML + CSS + JS in one file)
└── README.md
```

> The entire app is **self-contained in a single HTML file**.

---

## ▶️ How to Run

No setup required.

### Option 1 — Open directly

```bash
open index.html
```

### Option 2 — Use a local server (recommended)

```bash
# Python
python -m http.server

# Node
npx serve
```

Then open:

```
http://localhost:8000
```

---

## 🧪 Example Inputs

* `Data visualization empowers users to`
* `The quick brown fox jumps over`
* `Artificial intelligence will transform the`
* `In the beginning there was only`

---

## ⚙️ How It Works (Internals)

### 1. Precomputed Data

All model components are stored as static objects:

* `TOKENS`
* `EMBEDDINGS`
* `ATTENTION`
* `QKV`
* `MLP_OUT`
* `OUTPUT_PROBS`

### 2. Rendering Engine

Vanilla JS dynamically builds:

* Panels (Embedding, Attention, MLP, Output)
* Flow animations (SVG paths)
* Interactive UI components

### 3. Sampling Logic

Includes simplified implementations of:

* Softmax
* Temperature scaling
* Top-k / Top-p sampling

---

## 🎓 Learning Goals

This project helps you understand:

* How attention actually distributes weights
* What Q, K, V vectors represent
* Why Transformers scale so well
* How probabilities are generated for next tokens
* The role of temperature in generation

---

## 🚧 Limitations

* ❌ Not a real model (no inference)
* ❌ Uses simplified / approximated values
* ❌ Only a few example sequences
* ❌ Limited attention heads (2 visualized)

---

## 💡 Future Improvements

* Add real model inference (via API or WebGPU)
* Visualize all 12 attention heads
* Add custom text input
* Step-by-step animation mode
* Export attention maps
* Dark/light theme toggle

---

## 🙌 Inspiration

* Transformer architecture (Vaswani et al.)
* GPT-2 by OpenAI
* Educational visualizations from academia

---

## 📜 License

MIT License — free to use and modify.

---

## 👨‍💻 Author

Built as an educational tool to deeply understand Transformers through visualization.

---


