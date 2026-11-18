<div align="center">

# ⚡ OS PAGE REPLACEMENT SIMULATOR ⚡
### *Interactive Virtual Memory Management Visualization*

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](index.html)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](index.html)
[![CSS3](https://img.shields.io/badge/CSS3-Neon_Theme-00f3ff?style=for-the-badge&logo=css3&logoColor=white)](index.html)
[![Zero-Dependencies](https://img.shields.io/badge/Dependencies-0-00ff88?style=for-the-badge)](index.html)

<p align="center">
  A high-performance, single-file simulation engine designed with a <b>Dark Accent Neon UI</b> to visualize and benchmark Operating System Page Replacement Algorithms in real-time.
</p>

[✨ Launch Simulation](index.html) • [📖 Algorithms](#-supported-algorithms) • [🎮 Quick Start](#-quick-start) • [📊 Comparison Matrix](#-algorithm-comparison)

---

</div>

## 🌌 Overview

Modern operating systems use virtual memory where pages must be paged in from secondary storage into physical memory frames. When memory is full and a page fault occurs, a **Page Replacement Algorithm** decides which existing page to evict.

This simulator gives you complete visibility into this process with:
- 🕹️ **Interactive Step-by-Step Tracing** & **Auto Playback**
- 🎨 **Dark Neon Cyberpunk Theme** with live glow states (Hits in Neon Green, Faults in Hot Pink)
- 🧠 **Dynamic Step Explanations** detailing *why* each eviction or hit occurred
- 📊 **Multi-Algorithm Benchmark Matrix** for instant side-by-side comparison

---

## ⚡ Supported Algorithms

<details open>
<summary><b>1. FIFO (First-In, First-Out)</b></summary>
<br>

> *Replaces the page that arrived earliest in physical memory.*

- **Mechanism:** Maintains a queue of pages in memory ordered by arrival timestamp.
- **Characteristics:** Simple to implement, low overhead, but can suffer from **Belady's Anomaly** (where allocating more frames unexpectedly increases page faults).
</details>

<details>
<summary><b>2. LRU (Least Recently Used)</b></summary>
<br>

> *Replaces the page that has not been referenced for the longest time.*

- **Mechanism:** Examines backward memory access history.
- **Characteristics:** Excellent approximation of the Optimal algorithm; immune to Belady's Anomaly (stack algorithm).
</details>

<details>
<summary><b>3. MRU (Most Recently Used)</b></summary>
<br>

> *Replaces the page that was accessed most recently.*

- **Mechanism:** Targets the newest accessed page for eviction.
- **Characteristics:** Useful in access patterns where pages are scanned once and not referenced again immediately (e.g., sequential database scans).
</details>

<details>
<summary><b>4. Optimal (Belady's Min Algorithm)</b></summary>
<br>

> *Evicts the page that will not be accessed for the longest duration in future.*

- **Mechanism:** Looks forward into the reference stream to determine the furthest reference or pages never referenced again.
- **Characteristics:** Theoretically guarantees the minimum possible page fault rate; serves as the golden benchmark.
</details>

---

## 🎮 Quick Start

No installations, build steps, or servers required!

1. **Open in Browser:**
   Double click or open [`index.html`](file:///c:/Projects/Page-Replacement/index.html) in any modern web browser (Chrome, Edge, Firefox, Brave).
   
2. **Interactive Controls:**
   - **Preset Buttons:** Try pre-configured reference strings including standard textbook examples and Belady's Anomaly demo.
   - **Step Forward (⏭):** Watch memory frames update step-by-step.
   - **Auto Play (▶):** Run automatic playback with customizable speed slider.
   - **Compare All (📊):** View instant comparative analytics for all 4 algorithms with hit rates and fault counts.

---

## 📊 Algorithm Comparison

| Algorithm | Complexity | Looks | Belady's Anomaly? | Real-World Feasibility |
| :--- | :---: | :---: | :---: | :---: |
| **FIFO** | $\mathcal{O}(1)$ | Backward (Arrival) | ⚠️ Yes | Easy to implement |
| **LRU** | $\mathcal{O}(N)$ or Hardware Stack | Backward (Usage) | 🛡️ No | High with hardware help |
| **MRU** | $\mathcal{O}(N)$ | Backward (Usage) | ⚠️ Yes | Specialized workloads |
| **Optimal** | $\mathcal{O}(M \times N)$ | Forward (Future) | 🛡️ No | Theoretical benchmark only |

---

## 🎨 Theme & Tech Stack

- **Zero External Dependencies**: Pure Vanilla HTML5, CSS3, JavaScript ES6+
- **Typography**: Google Fonts (*Orbitron*, *Fira Code*, *Rajdhani*)
- **Color Palette**:
  - `Dark Canvas`: `#080b12`
  - `Neon Cyan`: `#00f3ff` (Primary HUD & Active Elements)
  - `Neon Green`: `#00ff88` (Page Hits)
  - `Hot Pink`: `#ff007f` / `#ff0055` (Page Faults & Evictions)
  - `Amber Glow`: `#ffaa00` (Eviction warnings & alerts)

---

<div align="center">
  <sub>Built for students, developers, and educators studying Operating System architectures.</sub>
</div>
