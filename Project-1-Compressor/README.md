# Project 1 -- Compressor Pressure Control

## Problem Statement
Maintain pressure in a receiver on a compressor application. Two pressure switches close at 90 PSI and 110 PSI. The system is controlled by one pump.

## My Solution
Wrote ladder logic that starts the pump when pressure drops to 90 PSI and stops it when pressure reaches 110 PSI, maintaining pressure within the operating range.

## Logic Elements Used
- Normally Closed (NC) and Normally Open (NO) contacts for pressure switch inputs
- Output coil for pump control
- Seal-in logic to maintain pump state between switch activations

## What I Learned
Understanding the difference between a start setpoint (90 PSI) and a stop setpoint (110 PSI) to prevent pump short-cycling. A direct PLC equivalent of a mechanical pressure switch.

## Difficulty
Medium
