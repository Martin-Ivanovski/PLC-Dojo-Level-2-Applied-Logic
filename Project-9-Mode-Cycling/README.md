# Project 9 -- Machine Mode and Function Cycling with Excel Data Export

## Problem Statement
Set up a machine that cycles continuously between two modes (Mode-1 and Mode-2), each running two functions (F1 and F2) for 10 seconds each. Store the current mode and function names as strings, count each complete cycle, and pull all data into Excel on demand via DDE.

## My Solution
Wrote a sequential state machine that cycles through Mode-1/F1, Mode-1/F2, Mode-2/F1, Mode-2/F2 on 10-second timer. Used string move instructions to update the current mode and function name registers for operator display. Implemented a string concatenation to combine the mode and function and string comparator to count each cycle. DDE connection to OpenOffice is currently in progress.

## Logic Elements Used
- Timer On Delay (TON) for 10-second function durations
- String move (MOV) instructions for mode and function name storage
- String Extract (AEX), ASCII String Compare (ASX) and String Concatenate (ACN) to get cycle each mode/function
- ASCII String Compare (ASX) and Add (ADD) to count each cycle. 
- DDE topic and item configuration for Excel connection (in progress)

## Current Status
- Core cycling logic (Mode-1/2, F1/F2 transitions): Complete
- String storage for mode and function names: Complete
- Cycle counter: Complete
- Excel DDE connection: In Progress

## What I Learned
String data handling for operator displays and sequential state machine design for multi-mode processes. The DDE integration is extending my understanding of how PLC data is exported to external applications for monitoring and reporting, which directly connects to MES used in industrial environments.

## Difficulty
Hard
