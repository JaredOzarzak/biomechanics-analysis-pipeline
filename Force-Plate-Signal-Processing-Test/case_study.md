# Force Plate Signal Processing Test

## Overview

This project demonstrates a basic test-engineering workflow for force plate data. The goal was to compare a noisy raw sensor signal against a filtered analysis signal, then extract key performance metrics from the cleaned signal.

## Purpose

Raw force data can be noisy and difficult to interpret directly. This workflow shows how sensor data can be checked, filtered, and converted into usable outputs for testing, troubleshooting, and performance analysis.

## Methods

A simulated force plate signal was created to represent a landing or contact event. Random sensor noise was added to create a raw signal. A zero-phase 4th-order Butterworth low-pass filter was then applied to clean the signal while keeping the timing aligned.

The notebook compares the raw and filtered signals visually, then calculates key performance metrics from the filtered signal.

## Key Metrics

- Peak force
- Loading rate
- Impulse
- Raw vs. filtered signal comparison
- Signal quality visualization

## Technical Stack

- Python
- NumPy
- Pandas
- SciPy
- Matplotlib
- Signal processing
- KPI extraction

## Outputs

- force_plate_signal_processed.csv
- force_plate_kpi_summary.csv
- Raw signal plot
- Raw vs. filtered signal plot
- KPI summary table

## Applied Value

This project shows how I approach test data: first by checking signal quality, then by applying a repeatable processing step, and finally by extracting metrics that can support testing decisions.

## Portfolio Relevance

For a test engineering role, this project demonstrates hands-on thinking around sensor data, repeatability, signal integrity, filtering, and turning raw measurement data into clear outputs.
