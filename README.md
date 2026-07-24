# Alpes Lasers Photon Wavelength & Energy Converter

A high-performance, precision-optimized, responsive single-page web utility that instantly converts photon metrics. Built for laser physicists, spectroscopy researchers, and engineers working in quantum cascade lasers (QCLs) and interband cascade lasers (ICLs).

Hosted at: [https://v1thesource.github.io/Photon_Converter/](https://v1thesource.github.io/Photon_Converter/)

---

## 🚀 Key Features

- **Bidirectional Real-Time Input:** Type any parameter (wavenumber, wavelength, energy, frequency) and see all others update instantly.
- **Gas Sensing Presets:** Instantly load the precise absorption lines for key molecules like $\text{CO}_2$, $\text{CH}_4$, $\text{CO}$, $\text{N}_2\text{O}$, $\text{H}_2\text{O}$, and $\text{NH}_3$.
- **Interactive EM Spectrum Visualizer:** Dynamically see the spectral region associated with your inputs (UV, Visible, Near-IR, Mid-IR, Far-IR, Terahertz).
- **Dual Constant Modes:**
  - **Alpes Classic Factor:** Employs the industry standard legacy conversion coefficient ($1\text{ eV} = 8065.544\text{ cm}^{-1}$ or factor $0.000123984193$).
  - **CODATA 2018:** Uses the latest ultra-high precision standards from the Committee on Data for Science and Technology (factor $0.0001239841984332$).
- **Customizable Decimal Precision:** Select from 4 to 10 decimal places, or use 'Auto' scientific mode.
- **Dark Mode Support:** Clean, high-contrast themes for laboratory and darkroom environments.
- **Calculation History:** Automatically keeps a log of your conversions for easy reference.
- **Copy-to-Clipboard:** Quick copy buttons on all inputs with responsive status states.

---

## 📐 Mathematical Conversions & Constants

The tool implements the following physical equations:

1. **Wavelength ($\mu\text{m}$) $\leftrightarrow$ Wavenumber ($\text{cm}^{-1}$):**
   $$\nu \ (\text{cm}^{-1}) = \frac{10,000}{\lambda \ (\mu\text{m})}$$

2. **Energy ($\text{eV}$) $\leftrightarrow$ Wavenumber ($\text{cm}^{-1}$):**
   $$\nu \ (\text{cm}^{-1}) = \frac{E \ (\text{eV})}{Factor}$$
   - *Alpes Classic Factor:* $0.000123984193\text{ eV}\cdot\text{cm}$
   - *CODATA 2018 Factor:* $0.0001239841984332\text{ eV}\cdot\text{cm}$

3. **Frequency ($\text{THz}$) $\leftrightarrow$ Wavenumber ($\text{cm}^{-1}$):**
   $$\nu \ (\text{cm}^{-1}) = \frac{f \ (\text{THz})}{0.0299792458}$$
   Where the denominator represents the speed of light in vacuum normalized to the units.

---

## 🛠️ Tech Stack & Architecture

- **Frontend:** HTML5, modern semantic structure.
- **Styling:** [Tailwind CSS CDN](https://tailwindcss.com/) featuring layout columns, flex components, interactive states, animations, custom fonts and dark mode classes.
- **Icons:** [Lucide Icons](https://lucide.dev/) for elegant visual indicators.
- **Math and Logic:** Vanilla JavaScript optimized with secure, float-safe validation, error boundary alerts, history limits, and dynamic DOM manipulation.

---

## 💻 Running Locally

Since this is a client-side SPA, you do not need to install any servers or build chains. Simply open `index.html` or `converter.html` in any web browser:

```bash
# Clone the repository
git clone https://github.com/v1thesource/Photon_Converter.git
cd Photon_Converter

# Open in your browser (macOS example)
open index.html
```

---

## 🧪 Automated Testing & Verification

To run headless browser test simulations, we use **Playwright**:

```bash
# Install dependencies
pip install playwright
playwright install chromium

# Run the verification script
python verify_converter.py
```
This tests preset interactions, bidirectional conversions, custom constants toggles, decimal formatting, and generates screenshots/videos of the CUJ (Critical User Journey).
