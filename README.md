# SevOne Sizing Sheets

## About

This repository contains Excel sizing sheets to estimate capacity requirements for SevOne-based solutions.

**Key Calculations:**
- Total monitored objects
- Indicators per second (IPS)
- NMS appliance / VM size recommendations

**Supported Solutions:**
- WiFi
- SDWAN
- Integrations (Mist, Meraki)

## Usage

### Step 1: Select Solution Sheet
📁 SevOne-Sizing-Sheets/
├── Mist_Sizing_sheet_8.1.xlsx
├── Meraki_Sizing_sheet_8.1.xlsx
└── SDWAN_sizing_sheet_all_vendors_8.1.0.xlsx


### Step 2: Input Your Data
1. Open the Excel sheet for your solution
2. Navigate to the relevant tab
3. **Fill yellow/highlighted input cells only:**
   - Number of devices/objects
   - Indicators per object
   - Polling interval
   - Solution-specific metrics (tunnels, clients, sites, etc.)

### Step 3: Review Outputs
**Calculated automatically:**
- ✅ Total Objects
- ✅ Indicators per Second (IPS)
- ✅ Recommended NMS Appliance Tier

**Do NOT edit formula cells** (white/gray background)

## What the Sheet Calculates

| **Input**                     | **Output**                  |
|-------------------------------|-----------------------------|
| Objects × Indicators/Object   | **Total Objects**           |
| Total Objects ÷ Poll Interval | **IPS (Indicators/Second)** |
| IPS + Objects                 | **NMS Appliance Tier**      |


> **Reference:** [SevOne NMS Hardware Guide](https://www.ibm.com/docs/en/sevone-nms)

## Assumptions & Notes

- Default retention: 7 days (adjust formulas if different)
- Polling assumes standard SevOne intervals (60s-300s)
- Cluster sizing: Multiple peers for >100k objects
- **Always validate** with official SevOne sizing methodology for production
