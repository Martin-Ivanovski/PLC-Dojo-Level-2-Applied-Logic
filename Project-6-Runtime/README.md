# Project 6 -- Plant Runtime Tracking

## Problem Statement
Track the cumulative runtime of a host plant. When the plant is running, it sends a signal. Measure and store the accumulated runtime. Include a reset button that clears the accumulated time to allow a fresh start.

## My Solution
Wrote retentive timer logic that accumulates runtime whenever the running signal is active. The timer retains its accumulated value when the running signal drops, preserving the total runtime across interruptions. A reset bit clears the accumulated value on demand.

## Logic Elements Used
- Retentive Timer On (RTO) for runtime accumulation
- Running signal input as the timer enable condition
- RES (Reset) instruction triggered by the reset button to clear accumulated time
- Accumulated time output register for display or downstream use

## What I Learned
The critical difference between standard TON timers and Retentive Timer (RTO) -- a TON resets when its enable goes false, while an RTO retains its accumulated value. Choosing the right timer type for the application is a fundamental PLC programming decision.

## Difficulty
Easy-Medium
