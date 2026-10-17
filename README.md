# Stellar Sagittarius: Weighing the Invisible

An observational astrophysics project dedicated to estimating the mass of Sagittarius A*—the supermassive black hole at the center of the Milky Way—by analyzing the orbital dynamics of the S-cluster stars (specifically the S2 star). 

By processing multi-instrument astrometric and radial velocity data, this computational pipeline reconstructs the orbital trajectories of these stars and applies Keplerian mechanics to derive the mass of the central gravitational body.

## Core Objectives
* **Data Harmonization:** Merge and standardize spatial and velocity observations from multiple independent astronomical instruments.
* **Spatial Visualization:** Construct projected 2D orbital planes from raw astrometric data to visualize the star's path across the sky.
* **Kinematic Analysis:** Map radial velocity variations over time to track the star's motion along the line of sight (towards and away from the observer).
* **Mass Estimation:** Utilize non-linear least squares fitting to model the orbit and calculate the invisible central mass.

## Observational Data
The analysis relies on real-world datasets compiled from multiple telescopes, categorized into two primary metrics:
* **Astrometry (Projected Position):** High-precision positional measurements from the NACO and SHARP instruments (`astrometry_NACO.csv`, `astrometry_SHARP.csv`).
* **Radial Velocity (Line-of-Sight Motion):** Spectroscopic velocity measurements from NACO, OSIRIS, and SINFONI (`velocity_NACO.csv`, `velocity_OSIRIS.csv`, `velocity_SINFONI.csv`).

## Technical Stack
* **Environment:** Python 3.8+, Jupyter Notebook
* **Data Handling:** Pandas, NumPy
* **Scientific Computation:** SciPy (`scipy.optimize.least_squares`)
* **Visualization:** Matplotlib

## Repository Architecture
Based on the current repository layout, all data files and notebooks are hosted in the root directory:

```text
Stellar_sagittarius/
├── astrometry_NACO.csv
├── astrometry_SHARP.csv
├── velocity_NACO.csv
├── velocity_OSIRIS.csv
├── velocity_SINFONI.csv
├── weighing_the_invisible.ipynb
└── weighing_the_invisible_comparative_stellar_orbits.ipynb
```

## Local Installation & Execution
Clone the repository to your local machine:
```bash
git clone https://github.com/AstronomyClub-VITStellar/Stellar_sagittarius.git
cd Stellar_sagittarius
```

Install the required Python dependencies:
```bash
pip install pandas numpy scipy matplotlib ipython
```

Launch the Jupyter environment and run the primary analysis notebook:
```bash
jupyter notebook weighing_the_invisible_comparative_stellar_orbits.ipynb
```

## Future Enhancements
* Implementation of general relativistic corrections (e.g., Schwarzschild precession) to refine the orbital model.
* Full 3D Keplerian orbit visualization mapping the exact geometry of the system.
* Robust parameter uncertainty and error propagation tracking.
* Expanding the pipeline to analyze multiple stars simultaneously for a constrained aggregate mass estimate.

## Author
**Sonakshi Jakhoria**  
B.Tech Computer Science and Engineering (Cybersecurity)  
*Technical Team VIT Stellar (Astronomy Club)*
