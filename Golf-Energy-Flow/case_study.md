# Golf Energy Flow

## Overview

This project analyzes simulated golf swing performance data to demonstrate how Python can be used to organize, normalize, visualize, and interpret sport-specific biomechanics variables. The goal is to show how rotational sequencing and energy-transfer concepts can be translated into a clean performance workflow for golf R&D, coaching, or fitting discussions.

## Dataset

This workflow uses a simulated dataset of 300 total swings from 30 golfers, with 10 swings per golfer. Players are separated into professional and amateur groups to compare differences in peak segment velocities, clubhead speed, timing, and consistency.

## Methods

I built a Python workflow that creates and analyzes golf performance data using player-level baselines and swing-to-swing variability. The pipeline calculates peak pelvis, torso, and lead-arm velocities, estimates clubhead speed, normalizes each player’s speed using Z-scores, and flags outlier swings based on individual consistency.

The workflow also visualizes group-level clubhead speed distributions and evaluates the relationship between pelvis peak velocity and clubhead speed to demonstrate an energy-flow style analysis.

## Key Outputs

- Created a 300-swing golf performance dataset using professional and amateur player groups.
- Calculated player-specific Z-scores to compare swing consistency relative to each athlete’s own baseline.
- Flagged stable and outlier swings using a Z-score threshold.
- Visualized clubhead speed distributions across groups.
- Compared pelvis peak velocity against clubhead speed to examine energy-transfer trends.
- Ranked players by an efficiency metric based on clubhead speed relative to pelvis peak velocity.

## Technical Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- Data visualization
- Simulated biomechanics dataset generation

## Applied Value

This project demonstrates how biomechanics and performance data can be structured into an organized analysis pipeline. Even with simulated data, the workflow shows how golf swing variables can be cleaned, normalized, visualized, and summarized in a way that supports coaching, fitting, and R&D-style decision-making.

## Portfolio Relevance

This project highlights my ability to connect sport biomechanics concepts with practical Python-based data workflows. The focus is not only on producing charts, but on creating a repeatable structure for analyzing athlete performance data and communicating the results clearly.
