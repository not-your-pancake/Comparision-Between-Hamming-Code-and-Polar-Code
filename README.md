# 📡 Bit Error Rate (BER) Simulation: Hamming Code vs. 5G Polar Code
(This has been prepared for my Digital Communication Course presentation)

An interactive Streamlit web sandbox that provides a side-by-side performance evaluation of two generations of channel coding: the classic **Hamming (7,4)** block code (1950s) and the modern **5G Polar Code (128,64)** (2000s). The simulation models data transmission over an Additive White Gaussian Noise (AWGN) channel using Binary Phase Shift Keying (BPSK) modulation.

---

## 🚀 Features & Controls

The application provides an interactive sidebar to manipulate simulation parameters in real-time:
* **Target Data Bits:** Controls the total payload size injected into the channel. Higher numbers smooth out statistical variance on the curves.
* **SNR Range (dB):** Adjusts the signal quality boundary limits ($0\text{ dB}$ representing a heavily degraded, noisy environment, scaling up to a clean $8\text{ dB}$ signal).

---

## 📊 Analytical Insights

* **Hamming (7,4) [Rate=0.57]:** Demonstrates a steady, linear decline in Bit Error Rate. Because it operates on a restricted 7-bit block window, its single-bit error correction ceiling limits its performance as signal quality scales.
* **Polar Code (128,64) [Rate=0.50]:** Exhibits a striking **"Waterfall Curve"**. At low SNR bounds ($2\text{--}4\text{ dB}$), the extreme noise prevents threshold calibration, resulting in a flat $50\%$ error rate. However, once past the $4\text{ dB}$ boundary, it triggers the channel polarization phenomenon—plunging straight down to a perfect $0$ error rate at $8\text{ dB}$.

---

## 🛠️ Installation & Execution

1.  **Clone the Repository:**
    ```bash
    # an example is shown just
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git) 
    cd your-repo-name
    ```

2.  **Install Required Dependencies:**
    ```bash
    pip install streamlit numpy matplotlib
    ```

3.  **Run the Web Application:**
    ```bash
    streamlit run app.py
    ```

---

## 🤝 Acknowledgments

This software implementation and its optimized analytical scripts were developed collaboratively with the assistance of advanced artificial intelligence models:
* **Gemini (Google):** For debugging, structuring the unrolled matrix calculations, and refining the Streamlit web architecture.
* **ChatGPT (OpenAI):** For establishing foundational layout elements and aiding in baseline scripting logic.
