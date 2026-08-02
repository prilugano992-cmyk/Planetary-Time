# 🪐 Planetary Time — Real Local Solar Time in 3D

An interactive 3D web application built with **Three.js** that simulates the planets of our Solar System and calculates the **real-time local solar time (LST)** for any clicked coordinate on a globe.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)

---

## ✨ Features

* **Interactive 3D Globes:** Smooth camera controls (orbit, pan, zoom) with high-detail canvas rendering and ambient starfield.
* **Real-time Solar Clock:** Click anywhere on any planet to calculate its local solar time mapped to a normalized 24-hour planet-centric clock (where 12:00:00 represents local solar noon).
* **Accurate Astrophysics Models:** Uses JPL/Standish J2000 Keplerian orbital elements and IAU planetary coordinate parameters to compute exact subsolar positions and axial tilts.
* **Time Controls:** Adjust time speed dynamically (1x real-time, 1s = 10 min, or 1s = 1 full solar day).
* **Technical Specs Panel:** Displays sidereal rotation period, solar day length, axial tilt angle, and rotation direction (prograde vs. retrograde).
* **Procedural Texture Fallback:** Includes procedural canvas texturing so the globes still render properly even if image assets fail to load.
* **System Info Modal:** Built-in technical documentation explaining the orbital mechanics and math behind the engine.
  
---

## 🔬 How It Works (Celestial Mechanics)

1. **Keplerian Orbit Calculation:** Heliocentric 3D positions are derived using mean Keplerian orbital elements calibrated to the J2000 epoch, solving Kepler's equation M = E - e * sin(E) for accurate anomalous angles.
2. **Body Rotation Framework:** IAU body-fixed rotation parameters (α₀, δ₀, W) dictate pole orientations, precession rates, and prograde/retrograde spin vectors.
3. **Subsolar Point Determination:** Projections map the relative solar vector onto the planet's surface to find the exact coordinates where the Sun is directly at the local zenith.
4. **Local Solar Time Mapping:** Local time calculates the angular difference between the user's selected point longitude and the current subsolar meridian.
   
---

## 📜 License

Distributed under the Apache 2.0 License. See `LICENSE` for more information.
