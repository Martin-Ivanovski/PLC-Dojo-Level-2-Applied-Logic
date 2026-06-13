# Project 3 -- Barcode Scanner Raw Materials Management

## Problem Statement
Manage 3 raw materials, each with its own part number. When a barcode is scanned, the program decodes a string in the format PPP-QQ:D where PPP is the part number, QQ is the quantity, and D is the direction (incoming or outgoing), then writes the data to the appropriate PLC registers.

## My Solution
Wrote ladder logic to receive the decoded barcode string, parse the part number, quantity, and direction components, and update the appropriate inventory registers for each of the 3 materials based on whether the transaction is incoming or outgoing.

## Logic Elements Used
- String comparison instructions to identify part number
- String manipulation to extract quantity and direction fields
- Math instructions (ADD for incoming, SUB for outgoing) applied to inventory registers
- Separate integer registers for each of the 3 material inventories

## What I Learned
String handling and parsing in PLC ladder logic. A skill directly applicable to MES integration, barcode-driven manufacturing systems, and any application where text data from an external device must be decoded and acted upon by the PLC.

## Why I Am Proud of This One
String manipulation in ladder logic is significantly more complex than standard bit and integer operations. Successfully parsing a formatted string into its components and routing the data correctly to three separate material registers was a genuine challenge.

## Difficulty
Hard
