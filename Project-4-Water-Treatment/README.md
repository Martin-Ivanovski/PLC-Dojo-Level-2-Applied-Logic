# Project 4 -- Water Treatment System Control Valve

## Problem Statement
Integrate a modular water treatment system into an existing host system. When the host calls for a cycle, a servo cycles a control valve through positions: Home, Fill (10 seconds), Drain (20 seconds), Flush (10 seconds), then back to Home. Cam-operated microswitches report the current valve position.

## My Solution
Wrote a sequential state machine using timer logic to control the valve cycle timing. Used microswitch inputs to confirm valve position at each stage before advancing. Implemented both bonus tasks: integer position reporting and reset/interrupt functionality.

## Logic Elements Used
- Timer On Delay (TON) for fill (10s), drain (20s), and flush (10s) timing
- Microswitch inputs for physical position confirmation at each stage
- Sequential state transitions gated on both timer completion and position confirmation
- Integer register N7:0 for position reporting (0=Home, 1=Fill, 2=Drain, 3=Flush, 4=Travelling)
- Bit B3:0/0 for reset/interrupt that aborts the cycle and returns valve to home

## Bonus Tasks Completed
- Bonus 1: N7:0 position reporting register (0=Home, 1=Fill, 2=Drain, 3=Flush, 4=Travelling)
- Bonus 2: B3:0/0 reset/interrupt button -- aborts the cycle from any state and returns to home

## What I Learned
Sequential state machine design in ladder logic -- controlling a multi-step process with defined timing, physical position feedback, and safe interrupt handling. The interrupt logic added significant complexity by requiring a controlled return-to-home from any active state without leaving the valve in an undefined position.

## Difficulty
Hard
