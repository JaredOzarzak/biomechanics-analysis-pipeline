# Jared Ozarzak: Biomechanics Data Projects

I'm an applied biomechanist in Columbus, OH. I work with force plate, motion capture, and EMG data, and this repository holds the Python notebooks behind my projects.

Each project started with a question I ran into while working with athletes or in the lab. They're ordered by how closely they relate to force plate and swing/jump testing.

---

## 1. Baseball vs. Softball Swing
A comparison of swing mechanics between baseball and softball hitters. I looked at how the body segments fire in sequence and where the movement patterns differ, and built visualizations to show the differences.

**Tools:** Python, Google Colab, Excel

## 2. Golf Energy Flow
An analysis of how power moves from the ground up through the body during a golf swing. I looked at rotational timing and how force and movement relate to swing efficiency.

**Tools:** Python, Google Colab, Excel

## 3. CMJ Biomechanics: Longitudinal Analysis
A longitudinal analysis of countermovement jump data across a three-month training block. The exports were European-style CSVs (semicolon delimiters, comma decimals), so I built a Python workflow to clean the files before analyzing them.

**Findings:** hip flexion angle changed by about 10°, knee movement stayed fairly stable, and overall power increased.

**Tools:** Python, pandas, Matplotlib

## 4. Force Plate Signal Processing & Data Quality Test
An evaluation of raw force plate data and how filtering changes it. I compared the raw signal against a zero-phase Butterworth filtered version, then extracted metrics from the cleaned data.

**Tools:** Python, NumPy, SciPy, pandas, Matplotlib

## 5. Sprint Prosthesis Biomechanics Pilot
A pilot study comparing sprint acceleration in a unilateral transtibial amputee wearing a running-specific prosthesis against an able-bodied control. I synchronized markerless kinematics, ground reaction force, and EMG to examine loading asymmetries and compensation patterns.

**Tools:** Python, SPM1D, Theia3D, AMTI force plates, Delsys EMG, Visual3D exports

## 6. Carbon-Plated vs. Training Footwear
A comparison of running gait in carbon-plated and traditional training footwear, covering stride characteristics, ground reaction forces, and lower-limb kinematics using both discrete and time-series measures.

**Tools:** Python, SPM1D, paired t-tests, pandas, NumPy, SciPy, Matplotlib

## 7. Pitcher Velocity Identification
A machine learning model that identifies pitchers likely to throw at high velocity, built for a technical assessment. I validated it with grouped cross-validation on 200+ subjects so no athlete appeared in both the training and test sets.

**Tools:** Python, scikit-learn, XGBoost

---

## Equipment and Software
- **Force plates:** AMTI, VALD
- **Motion capture:** Qualisys, Theia3D (markerless)
- **EMG:** Delsys
- **Analysis:** Python (pandas, NumPy, SciPy, Matplotlib, Seaborn, SPM1D), MATLAB, Visual3D, Excel

## Contact
Jared Ozarzak · Columbus, OH · [LinkedIn](https://linkedin.com/in/jared-ozarzak)
