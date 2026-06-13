# Project 8 -- Vacuum Control Without PID

## Problem Statement
Maintain a vacuum setpoint of 15 in/Hg in a system with rapidly changing environmental conditions. Sensor range is 0 to 30 in/Hg. Constraint: a PID controller cannot be used. Write custom control logic to speed up or slow down a pump to attain and maintain the setpoint.

## My Solution
Wrote a custom closed-loop control algorithm in ladder logic that continuously compares the current vacuum reading to the 15 in/Hg setpoint and adjusts the pump speed output accordingly.

## Logic Elements Used
- Analog input scaled to 0 to 30 in/Hg range
- SUB instruction to calculate error (setpoint minus actual)
- ADD and SUB instructions to increment or decrement pump speed output register
- Upper and lower limit checks to keep output within valid pump speed range

## What I Learned
Custom closed-loop control logic built from first principles -- implementing the measure, compare, correct cycle manually without relying on a PID instruction block. This deepened my understanding of what PID controllers do internally and how feedback control works at the logic level.

## Difficulty
Hard
