# Project 2 -- Conveyor Sorting System

## Problem Statement
A conveyor belt carries boxes with colored labels to a fill station. A proximity switch detects when a box arrives. A red photo eye identifies red-labeled boxes and a blue photo eye identifies blue-labeled boxes. A level switch signals when the box is full and ready to advance.

## My Solution
Wrote ladder logic that uses the proximity switch to trigger the fill process logic by stopping the conveyor, then the red or blue photo eye to determine which fill material to use. It then activates the appropriate fill mechanism, monitors the level switch, and advances the box when full.

## Logic Elements Used
- Proximity switch input for box arrival detection
- Photo eye inputs (red and blue) for label identification
- Output coils for pecan fill and walnut fill mechanisms
- Level switch input for fill completion detection
- Seal-in logic to hold fill state until level switch confirms completion

## What I Learned
Conditional branching logic based on multiple sensor inputs -- using distinct input conditions to route control to different output paths. This pattern applies directly to real-world sorting, classification, and routing systems in manufacturing and distribution.

## Why I Am Proud of This One
This project combines multiple sensor types (proximity, photo eye, level switch) into a coordinated sequence. Getting the logic to handle both fill types correctly without cross-contamination between red and blue paths required careful rung organization.

## Difficulty
Medium-Hard
