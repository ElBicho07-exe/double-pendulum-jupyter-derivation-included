Absolutely — here is a **clean, professional README.md** you can directly drop into your project folder.
It’s written at a **student–researcher level**: honest, clear, and impressive without exaggeration.

---


# Double Pendulum Simulation (Python)

A **physics-accurate double pendulum simulation** built from **first principles** using  
**Lagrangian mechanics**, **symbolic computation**, and **numerical integration**.

The project derives the equations of motion symbolically, solves them numerically, and produces
**smooth, dark-mode animations** exported as **MP4 and GIF** files.

This is **not a hard-coded demo** — all equations are derived programmatically.

---

## Physics Background

The double pendulum consists of:
- Two point masses
- Two rigid, massless rods
- Motion constrained to a plane
- Gravity as the only external force

The system is:
- **Nonlinear**
- **Coupled**
- **Chaotic**

Small changes in initial conditions lead to drastically different trajectories.

### Method Used
- Generalized coordinates: θ₁(t), θ₂(t)
- Lagrangian: **L = T − V**
- Euler–Lagrange equations
- Conversion to first-order ODEs
- Numerical integration with adaptive Runge–Kutta

---

## Key Features

- ✅ Equations derived symbolically using **SymPy**
- ✅ No small-angle approximations
- ✅ Adaptive numerical integration (`solve_ivp`)
- ✅ Energy-consistent dynamics
- ✅ Smooth animation via uniform resampling
- ✅ Dark mode visualization
- ✅ MP4 and GIF export
- ✅ Works in **Jupyter Notebook** (export-focused)

---

##  Project Structure

```

.
├── double_pendulum_dark.ipynb   # Jupyter notebook (main work)
├── double_pendulum_dark_demo.mp4     # Exported video (generated)
├── double_pendulum_dark_demo.gif     # Exported GIF (generated)
└── README.md

````

---

##  Requirements

Install Python dependencies:

```bash
pip install numpy scipy sympy matplotlib pillow
````

### Optional (for MP4 export)

Install **FFmpeg** and ensure it is on PATH:

```bash
ffmpeg -version
```

If FFmpeg is unavailable, the project **automatically supports GIF export** using Pillow.

---

## ▶ How to Run (Jupyter Notebook)

1. Open the notebook:

   ```bash
   jupyter notebook
   ```

2. Run cells **top to bottom**

3. The notebook will:

   * Derive equations
   * Solve the system
   * Render animation frames
   * Save:

     * `double_pendulum_dark.mp4`
     * `double_pendulum_dark.gif`

 **Note:**
Inline animation playback in Jupyter is unreliable.
This project intentionally **exports video files instead** for correctness and stability.

---

##  Output

* **MP4**

  * High quality
  * Smooth 60 FPS
  * Best for presentations and portfolios

* **GIF**

  * Short preview
  * Easy sharing
  * Larger file size

---

##  Numerical Details

* Integration method: Adaptive RK45
* Tolerances:

  * `rtol = 1e-9`
  * `atol = 1e-9`
* Time resampling used **only for rendering**
* Physics integration remains untouched

---

##  Important Notes

* Animation does **not** recompute physics
* All motion comes from solver output
* Chaos observed is **physical**, not numerical noise
* Energy conservation can be checked independently

---

##  What This Project Demonstrates

* Translating theoretical physics → executable code
* Proper separation of:

  * Physics
  * Numerics
  * Visualization
* Good scientific programming practices
* Understanding (not memorization) of chaos

---

##  Possible Extensions

* Energy-colored trajectory
* Phase-space plots
* Poincaré sections
* Symplectic integrators
* Side-by-side chaos divergence
* Damping or driven pendulum
* GUI controls

---

##  Author Notes

This project was built as a **learning-focused simulation**, prioritizing:

* Correct physics
* Transparent derivation
* Numerical integrity

It is suitable for:

* Physics / engineering students
* Computational physics portfolios
* Demonstrating chaos theory concepts

*“The goal was not to make it look cool —
the goal was to make it true.”*
