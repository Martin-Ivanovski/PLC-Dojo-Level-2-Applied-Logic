# Project 10 -- Pump Control with HOA and Dual-Bit Alarms

## Problem Statement
Control a pump on a continuous 30 second run / 10 second stop cycle. Protect the pump with a flow switch and a pressure sensor. The cycle terminates on either fault condition: no flow detected within 5 seconds of the pump starting, or pressure exceeding 30 PSI for 5 seconds. Both faults raise dual-bit alarm and notification indicators. The pump includes Hand-Off-Auto (HOA) control. HAND energizes the pump only while the button is actively pressed, and the pump returns to its prior mode (OFF or AUTO) once released. While any alarm is active, the pump cannot enter or remain in AUTO mode, only OFF or HAND.

## My Solution
Built a continuous cyclic timer for the 30 second run / 10 second stop sequence. Added two independent fault monitoring branches, each using a time-delayed comparator so a fault is only declared after the condition persists for the full 5 second window rather than on a momentary reading. Each fault sets a dual-bit alarm pair (active alarm bit and operator notification bit) and forces the pump out of AUTO. Built HOA selector logic where HAND is a momentary override that energizes the pump directly while pressed, and on release the logic restores whichever mode (OFF or AUTO) was active before HAND was pressed. Designed the system so HAND remains available even during an active alarm, allowing a technician to manually run the pump for diagnostic or clearing purposes while preventing the automatic cycle from resuming until the alarm is cleared.

## Logic Elements Used
- Cyclic Timer On Delay (TON) pair for the continuous 30 second run / 10 second stop sequence
- Comparator instructions for the 30 PSI pressure threshold
- Scale with Parameters (SCP) for analog pressure sensor input scaling
- Time-delayed fault confirmation timers (5 second qualification window for both flow loss and overpressure)
- Dual-bit alarm architecture (active alarm bit plus operator notification bit) for each fault condition
- Hand-Off-Auto (HOA) selector logic with momentary HAND override and mode-restore on release
- Interlock logic preventing AUTO mode entry or continuation while any alarm bit is active

## What I Learned
Designing fault logic that requires a condition to persist for a defined time window, rather than triggering on a single scan, is essential in real industrial systems to avoid nuisance trips from momentary sensor noise. The HOA momentary-HAND-with-mode-restore behavior required tracking the prior state before the override, which is a different pattern than a standard maintained selector switch.

## Why This Was Hard
This project combines four distinct logic systems into one coordinated program: cyclic timing, dual independent time-qualified fault detection, dual-bit alarm and notification handling, and momentary HOA override with state memory. Getting all four to interact correctly, especially making sure the alarm interlock properly blocked AUTO without also blocking the legitimate HAND override, took careful rung sequencing.

## Difficulty
Very Hard
