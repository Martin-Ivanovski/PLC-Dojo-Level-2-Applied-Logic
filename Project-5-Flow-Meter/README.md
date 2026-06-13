# Project 5 -- Digital Rotameter Oil Flow Measurement

## Problem Statement
Measure oil flowing through a pipeline using a digital rotameter that sends one pulse for every 6.3 gallons (k-factor). The rotameter is connected to a bit address controlled by a timer. Create timer logic that pulses the bit every 12 seconds, accumulates the pulse count, calculates gallons, and stores the flow rate updated every 12 seconds.

## My Solution
Wrote timer logic that pulses the rotameter bit on a 12-second interval. Used a counter to accumulate pulses, multiplied the count by the k-factor (6.3 gallons per pulse) to calculate total gallons, and stored the flow rate to a float address updated every 12-second cycle.

## Logic Elements Used
- Timer On Delay (TON) for 12-second interval pulsing
- Counter Up (CTU) to accumulate rotameter pulses
- Multiply instruction (pulse count x 6.3) for gallon calculation
- Float register for flow rate storage
- Counter reset on each 12-second update cycle

## What I Learned
Pulse-based measurement and k-factor scaling -- translating discrete pulses into engineering units using multiplication. This technique is used in flow metering, utility metering, and any application where a sensor outputs pulses proportional to a physical quantity.

## Difficulty
Medium
