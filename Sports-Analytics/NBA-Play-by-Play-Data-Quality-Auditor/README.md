# NBA Play-by-Play Data Quality Auditor

**Focus:** Basketball Operations, Data Validation, Stats Auditing, Sports Analytics  
**Tools:** Python, pandas, NumPy, Matplotlib

## Project Overview

This project simulates a live NBA play-by-play data feed and audits it for common data quality issues that could affect basketball operations, official stat review, analytics reporting, and downstream performance models.

The goal is to show how Python can be used to automatically flag errors in large sports data feeds before analysts, coaches, or front offices use the data.

## What This Project Does

The auditor reviews a simulated NBA game feed and flags:

- Invalid scoring values
- Missing player attribution
- Player-team mismatches
- Duplicate event IDs
- Clock sequence errors
- Possession logic issues
- Running score inconsistencies

## Key Result

Processed 700+ simulated NBA play-by-play events and automatically detected scoring, attribution, possession, clock, and statistical inconsistencies through rule-based validation checks.

## Why This Matters

Sports analytics depends on clean data. If play-by-play data contains errors, then lineup analysis, possession models, scouting reports, broadcast graphics, betting feeds, and internal dashboards can all be affected.

This project demonstrates an operational analytics mindset: before using the data, validate it.

## Skills Demonstrated

- Python data analysis
- pandas workflow design
- Data validation logic
- Basketball operations thinking
- Automated audit reporting
- Error flagging and review workflows
- Sports data quality control
