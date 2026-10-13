# Baseball vs. Softball Swing Comparison

## Overview
A comparison of swing mechanics between baseball and softball hitters, focused on how the body transfers energy from the ground up through the hips and trunk. Completed as part of graduate biomechanics coursework (KIN 6016).

## Data
Visual3D exports from motion capture (300 Hz) and ground reaction force data for five baseball swings and five softball swings.

## Methods
- Parsed the Visual3D exports in Python (pandas, NumPy), pulling both time-series signals and single-value metrics from each file
- Time-normalized every swing to 101 points (0-100% of the swing) using linear interpolation
- Smoothed pelvis and thorax angular velocity with a 4th-order, zero-lag Butterworth low-pass filter (15 Hz cutoff), applied to each swing individually
- Plotted mean ± SD curves for each sport and ran a two-sample SPM t-test (spm1d, two-tailed, α = 0.05) to mark the parts of the swing where the groups differ
- Calculated per-swing and group-mean discrete metrics

## Variables
- **Kinematics:** pelvis angular velocity, thorax angular velocity
- **Energy flow (joint transfer power):** back hip, lead hip, L5S1
- **Discrete metrics:** bat speed, peak back leg ground reaction force, and energy transfer at the back hip, lead hip, and L5S1

## Results (group means)
| Metric | Baseball | Softball |
|---|---|---|
| Bat speed (m/s) | 32.6 | 24.3 |
| Peak back leg GRF (N) | 757 | 625 |
| Back hip energy transfer (J) | 44.5 | 3.0 |
| Lead hip energy transfer (J) | 365.7 | 406.6 |
| L5S1 energy transfer (J) | 1032.0 | 1049.0 |

Baseball swings showed higher bat speed, higher peak back leg force, and much more energy transfer through the back hip. Lead hip and L5S1 energy transfer were similar between the two sports.

## Limitations
Five swings per group, so this is a descriptive comparison and the differences shouldn't be generalized to all baseball and softball hitters.

## Technical Stack
Python, Google Colab, pandas, NumPy, SciPy, spm1d, Matplotlib, Visual3D exports
