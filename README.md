# Jared Ozarzak: Biomechanics Data Projects

I'm an applied biomechanist in Columbus, OH. I work with force plate, motion capture, and EMG data, and this repository holds the Python notebooks behind my projects.

Each project started with a question I ran into while working with athletes or in the lab. They're ordered by how closely they relate to force plate and swing/jump testing.

---

## 1. Baseball vs. Softball Swing
A comparison of baseball and softball swing mechanics, completed as part of graduate biomechanics coursework. Using Visual3D exports, I compared pelvis and thorax angular velocity and joint transfer power at the back hip, lead hip, and L5S1 across five swings per sport, with SPM t-tests to show where the curves differ. Baseball swings averaged a bat speed of 32.6 m/s versus 24.3 m/s for softball, with higher peak back leg force (757 N vs. 625 N).

**Tools:** Python, Google Colab, SPM1D, Matplotlib, Visual3D exports

## 2. Golf Energy Flow
An analysis of how power moves from the ground up through the body during a golf swing. I looked at rotational timing and how force and movement relate to swing efficiency.

**Tools:** Python, Google Colab, Excel

## 3. CMJ Biomechanics: Longitudinal Analysis
A longitudinal analysis of countermovement jump data across a three-month training block. The exports were European-style CSVs (semicolon delimiters, comma decimals), so I built a Python workflow to clean the files before analyzing them.

**Findings:** hip flexion angle changed by about 10°, knee movement stayed fairly stable, and overall power increased.

**Tools:** Python, pandas, Matplotlib

## 4. Sprint Prosthesis Biomechanics Pilot
A pilot study from graduate coursework comparing sprint acceleration in a unilateral transtibial amputee wearing a running-specific prosthesis against an able-bodied control (five trials each, collected by my lab group). I used SPM t-tests on ground reaction force and EMG across the stance phase, plus t-tests on peak joint angles. The intact limb showed higher mid-stance force, more muscle activation, and reduced hip and knee flexion, while the prosthetic limb showed delayed force production in late stance.

**Tools:** Python, SPM1D, Theia3D, AMTI force plates, Delsys EMG, Visual3D exports

## 5. Carbon-Plated vs. Training Footwear
A comparison of running gait in carbon-plated and traditional training footwear, covering stride characteristics, ground reaction forces, and lower-limb kinematics using both discrete and time-series measures.

**Tools:** Python, SPM1D, paired t-tests, pandas, NumPy, SciPy, Matplotlib

## 6. Five-Year Velocity Projection: 2025 FCL Pitchers
A technical assessment projecting which 2025 FCL pitcher is most likely to throw the hardest fastball in five years. I trained a random forest on 8,981 pitches from 203 pitchers, validated it with pitcher-grouped cross-validation so no pitcher appeared in both training and testing, and checked how stable the rankings were with a bootstrap. The model's R² was low (0.07), so I presented the results as tiers rather than exact predictions.

**Tools:** Python, pandas, NumPy, scikit-learn, Matplotlib

---

## Equipment and Software
- **Force plates:** AMTI, VALD
- **Motion capture:** Qualisys, Theia3D (markerless)
- **EMG:** Delsys
- **Analysis:** Python (pandas, NumPy, SciPy, Matplotlib, Seaborn, SPM1D), MATLAB, Visual3D, Excel

## Contact
Jared Ozarzak · Columbus, OH · [LinkedIn](https://linkedin.com/in/jared-ozarzak)
