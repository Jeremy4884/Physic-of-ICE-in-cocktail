# Physic-of-ICE-in-cocktail

> **Interactive 3D Simulation & Scientific Analysis of Ice Crystallography, Geometry, and Thermodynamics in Cocktails**

An interactive, web-based 3D physics simulation exploring the crystallization of hexagonal ice ($I_h$), cocktail glassware geometry, and the thermodynamic kinetics of shaking versus stirring.

---

## 🧊 Overview & Interactive Modules

### 1. Types of Cocktail Ice in the Glass (`Ice in the Glass`)
- **3D Glassware & Ice Simulation**: Real-time rendering of signature bar ice shapes with realistic refraction, surface recession, and melting dynamics:
  - **Collins Spear** (1.25 × 5 in): Highball column minimizing surface area and nucleation sites to preserve carbonation in drinks like *Gin & Tonic* and *Highball*.
  - **Ice Sphere** (2.25 in): Minimal surface-to-volume ratio ($A/V$), providing slow dilution for spirit-forward drinks like *Whisky on the Rocks*.
  - **Pebble Ice**: Porous, crushed ice nuggets providing flash chilling and high meltwater for *Mint Julep*, *Mojito*, and *Tiki* cocktails.
  - **King Cube** (2 × 2 in): Dense, slow-melting block for *Old Fashioned* and *Negroni*.
  - **Standard Cube (Kold-Draft)** (1.25 × 1.25 in): The universal workhorse balancing chilling and dilution for mixing.
- **Nucleation Site Analysis**: Interactive bubble simulation showing why multi-cube drinks go flat faster than single clear spears.

### 2. Crystallography of Hexagonal Ice $I_h$ (`Freezing Simulation`)
- **Zone Refining & Impurity Rejection**: Earth's ice crystallizes into hexagonal ice ($I_h$) with an equilibrium partition coefficient $k < 10^{-4}$ for dissolved gases ($O_2, N_2, CO_2$) and minerals ($Ca^{2+}, Mg^{2+}, Na^+$).
- **Omnidirectional Freezing**: Heat escapes through all 6 faces, trapping micron-scale air voids and mineral inclusions in the center. Causes **Mie scattering** (milky white opacity) and severe internal thermal stresses ($+9\%$ volume expansion).
- **Directional Freezing**: Insulated walls force heat extraction strictly through the top. At controlled freezing front velocities (1–3 mm/h), impurities are pushed ahead of the planar front into the bottom liquid, achieving monocrystalline/large-grain clear ice with **80–95% lower TDS**.

### 3. Shaking vs. Stirring Kinetics (`Shaking vs Stirring`)
- **Thermodynamic Energy Balance**: Calibrated against empirical data from **Dave Arnold (*Liquid Intelligence*)** and Blagden's law of freezing point depression:
  $$\frac{dQ}{dt} = h \cdot A(t) \cdot (T_{liquid} - T_{fp})$$
  $$\Delta H_f \approx 333.6\text{ J/g}$$
- **Fundamental Mixology Rule**: *"There is no chilling without dilution, and no dilution without chilling."*
- **Shaking ($h \approx 3,600\text{ W/m}^2\text{K}$, Ice Shattering)**: Rapid turbulent cavitation approach to thermal equilibrium plateau in **10–12 s** at $-4^\circ\text{C}$ to $-7^\circ\text{C}$ with ~33–36% dilution and aeration foam.
- **Stirring ($h \approx 480\text{ W/m}^2\text{K}$, Laminar Flow)**: Gradual chilling slope; standard 30 s stir terminates at $-1.5^\circ\text{C}$ to $+2^\circ\text{C}$ (~25–28% dilution) preserving clarity. Requires 90–120 s to match a 12 s shake.
- **Dual Real-time Charts & Auto-Solver**: Live 2D canvas temperature and dilution curves, cocktail selection (*Daiquiri*, *Manhattan*, *Negroni*), initial ice temperature ($-18^\circ\text{C}$, $-5^\circ\text{C}$, $0^\circ\text{C}$), pre-chilled vessel toggles, and *"Stir until it matches the shake"* auto-calculator.

---

## 🎨 Aesthetics & Sound

- **Minimalist Studio Lighting**: Custom HDR studio environment maps with clearcoat wet sheen, Fresnel rim illumination, and glints.
- **Dark Mode & Light Mode**: Seamless theme switching with persistent state and eye-friendly contrast.
- **Procedural Kissaten Jazz (喫茶店ジャズ)**: 100% self-contained Web Audio API jazz trio synthesizing Rhodes piano (ii–V–I comping), walking acoustic bass, swinging ride cymbal, soft brush snare swirl, and vintage vinyl crackle.
- **Mobile Responsive Design**: Fluid bottom drawer / collapsible controls, touch-friendly OrbitControls, horizontal carousel selectors, and non-overlapping overlay cards.

---

## 🚀 Getting Started

Simply open `index.html` in any modern web browser, or serve locally:

```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .
```

Open `http://localhost:8080` in your browser.

Direct tab navigation:
- `index.html` — Tab 1: Ice in the Glass
- `index.html?tab=freeze` — Tab 2: Freezing Simulation
- `index.html?tab=mix` — Tab 3: Shaking vs Stirring

---

## 📚 References & Mixology Science
1. **Dave Arnold**, *Liquid Intelligence: The Art and Science of the Perfect Cocktail*, W. W. Norton & Company, 2014.
2. **Dave Arnold**, *Cooking Issues* — Shaking and dilution kinetics experiments.
3. **CRC Handbook of Chemistry and Physics**, *Concentrative Properties of Aqueous Solutions: Freezing-Point Depression of Ethanol-Water Solutions*.
4. **Difford's Guide**, *Shaking cocktails: Time, equilibrium, and dilution*.
