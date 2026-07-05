# daq-keithley-iv

> LabVIEW VIs and TSP scripts for automated IV (current-voltage) characterization of photovoltaic samples using the Keithley 2600 Series SourceMeter.

![Language](https://img.shields.io/badge/LabVIEW-FFDB00?style=flat&logo=labview&logoColor=black)
![Language](https://img.shields.io/badge/TSP-Keithley%20Script%20Processor-lightgray?style=flat)
![Domain](https://img.shields.io/badge/Domain-Hardware%20DAQ-lightgray?style=flat)

## What It Does

Automates IV sweep measurements on photovoltaic and thin-film material samples using the Keithley 2600B SMU (Source Measure Unit). Two implementations are included:

- **TSP scripts** — Keithley's built-in scripting language runs directly on the instrument, enabling standalone operation without a host PC
- **LabVIEW VIs** — graphical instrument control and real-time data visualization running on a host workstation

Built March–August 2021 as part of research into [`photovoltaic material characterization`](https://pubs.acs.org/doi/full/10.1021/acsaem.4c02470).

## Transferable Skills



This project demonstrates:

- **Dual-interface instrument control** — implementing the same measurement logic in both an embedded scripting language (TSP) and a graphical environment (LabVIEW) shows the ability to adapt to different tooling constraints, the same flexibility needed when working across CLI, GUI, and API-driven infrastructure tools
- **Embedded scripting** — TSP scripts run on the instrument's own processor, similar in concept to firmware-level automation or running scripts directly on network devices (Cisco EEM, vendor CLIs)
- **Real-time data visualization** — LabVIEW front panels display live IV curves during sweeps, the same principle behind operational dashboards in IT monitoring
- **Measurement system integration** — this instrument worked in coordination with the PSU and spectrum analyzer, requiring synchronized operation across multiple devices — directly analogous to multi-tool orchestration in DevOps pipelines

## Hardware

- **Instrument:** Keithley 2600B Series SourceMeter (SMU)
- **Interfaces:** TSP (embedded) + GPIB/USB via LabVIEW
- **Languages:** TSP (Lua-based), LabVIEW G

## Context

The third instrument in a coordinated noise and electrical characterization pipeline for photovoltaic and RF material samples at MSc level. The SMU applied bias voltages and measured resulting currents to generate IV curves used to extract material electrical parameters.

Equipment Manual 📖: https://www.tek.com/en/keithley-source-measure-units/smu-2600b-series-sourcemeter-manual-8
