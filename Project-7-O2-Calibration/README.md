# Project 7 -- O2 Sensor Calibration System

## Problem Statement
Monitor oxygen concentration at the bottom of a coal mine -- a life-safety critical application. The O2 sensor reads 0% to 40% but degrades over time and requires calibration against known reference gases: 0% O2 (zero calibration) and 30% O2 (span calibration). Implement logic to calibrate the sensor and maintain accurate readings.

## My Solution
Wrote calibration logic that applies zero and span correction to the raw sensor signal. Used the known calibration gas values to calculate offset and gain correction factors, adjusting the sensor output to accurately represent true O2 concentration. Implemented the calibration as an on-demand operator-triggered process.

## Logic Elements Used
- Analog input scaling for raw sensor signal
- Zero calibration: offset correction using the 0% reference gas
- Span calibration: gain correction using the 30% reference gas
- Math instructions (SUB for offset, DIV and MUL for gain scaling)
- Float registers for calibrated output storage
- Operator trigger inputs for initiating zero and span calibration sequences

## What I Learned
Sensor calibration mathematics in PLC logic -- applying zero offset and span gain correction to analog inputs is a fundamental skill in process control and industrial instrumentation. This pattern applies to any environment using analog sensors that drift over time, including temperature transmitters, pressure transducers, and flow meters.

## Why This Project Matters
Accurate O2 monitoring in a mine is a direct safety requirement. Sensor drift without calibration could produce false readings that fail to warn of dangerous low-oxygen conditions. This project reinforced the real-world consequences of getting instrumentation logic right and the engineering responsibility that comes with safety-critical applications.

## Difficulty
Hard
