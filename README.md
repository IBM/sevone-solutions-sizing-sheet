<!-- This should be the location of the title of the repository, normally the short name -->
# SevOne Sizing Sheets

<!-- Build Status, is a great thing to have at the top of your repository, it shows that you take your CI/CD as first class citizens -->
<!-- [![Build Status](https://travis-ci.org/jjasghar/ibm-cloud-cli.svg?branch=master)](https://travis-ci.org/jjasghar/ibm-cloud-cli) -->

<!-- Not always needed, but a scope helps the user understand in a short sentance like below, why this repo exists -->
## About

This sizing sheet helps estimate capacity requirements for SevOne-based solutions.
It is designed to calculate:

Total monitored objects

Indicators per second (IPS)

High-level guidance for selecting appropriate SevOne NMS appliance / VM sizes

The sheet can be used for multiple solution types (for example, SNMP-based monitoring, integrations such as Mist, or other data sources) as long as you know the key volume and polling characteristics of the deployment.

This guide is based on general principles from SevOne NMS cluster sizing, production hardware configuration, and appliance capacity guidelines and is intended as a quick, practical aid for pre-sales, architects, and implementation teams.

<!-- A more detailed Usage or detailed explaination of the repository here -->
## Usage


Open the Excel sizing sheet.

Navigate to the tab that corresponds to your solution or integration (for example, “Mist”, “SNMP Core”, or “Custom Integration”).

Fill in all highlighted input cells:

Number of devices / objects

Average indicators per object (per technology or object type)

Polling interval (in seconds)

Any solution-specific counts (for example, tunnels, clients, flows, sites, or controllers)

Review the calculated outputs:

Total objects

Total indicators per second (IPS)

Any derived metrics used for capacity (for example, flows per second if applicable)

All colored or highlighted cells are user inputs; non-highlighted cells contain formulas and should not be edited.

What the Sheet Calculates
The sizing sheet computes:

Total number of monitored objects for the solution

Total indicators per second (IPS) based on:

Number of objects

Average indicators per object

Polling interval

Optional, solution-specific metrics (for example, tunnel counts, number of clients, or other derived objects)

These values are then used to map to SevOne NMS appliance sizes using generic capacity guidance (for example, IPS thresholds and object limits per appliance tier).

Once you have:

Total objects

Total indicators per second (IPS)

Use the “NMS Sizing” or “Appliance Mapping” section of the sheet to:

Identify the recommended NMS appliance / VM tier (for example, vPAS5k, vPAS20k, vPAS60k, vPAS100k, etc.).

Understand approximate:

Maximum supported objects

Maximum IPS

Typical storage needs (based on default retention)

If your calculated IPS or object count exceeds a single appliance’s capacity, you may need:

Multiple NMS peers in a cluster, or

A higher-tier appliance than originally planned

Always verify final appliance selection against the latest official SevOne hardware and instance-type documentation.

[issues]: https://github.com/IBM/repo-template/issues/new
