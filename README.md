# **GTCC PLC Lab Station Documentation Package**

This repository contains the **technical documentation** for **a PLC Lab Station** in the GTCC Mechatronics program.
It documents the **hardware platform only** (PLC, HMI, PSU, I/O modules, terminals, wiring, and network settings).
The station does **not** include pre-wired field devices or pre-programmed logic.

---

## **Scope**

Document the **physical configuration, wiring, power distribution, and network setup** of a singular PLC Lab Training Station, consisting of a dual-vendor PLC training workstation including **Allen-Bradley (Rockwell) ControlLogix + CompactLogix remote I/O** and **Siemens S7-1500 + SIMATIC ET 200 remote I/O**, plus an **Allen-Bradley PanelView 5310 HMI**, 24 VDC power subsystem, DIN-rail infrastructure, and lab Ethernet connectivity. 


## 1) Rockwell / Allen-Bradley Stack

**ControlLogix Chassis (Primary Controller)**

* 1756-series ControlLogix 5580 CPU
* DI/DO modules in local chassis
* Backplane + chassis PSU

**CompactLogix 5069 Remote I/O**

* **5069-AENTR** Ethernet adapter
* 5069-IB16 (DI), 5069-OB16 (DO)

**PanelView 5310 HMI**
* 10.4" industrial HMI (EtherNet/IP to controller)


## 2) Siemens Stack

**S7-1500 Rack (Primary Siemens Controller)**

* CPU 15xx (exact model TBD)
* DI/DO modules in local rack
* Profinet interface on CPU

**SIMATIC ET 200 Remote I/O**

* **Profinet adapter/interface**
* **CM 4×IO-Link master** (IO-Link channel expansion)
* DI/DO modules on ET 200 node

> Siemens and Rockwell systems are mounted on the same panel but are **independent** control domains for training.

## 3) Power & Panel Infrastructure

* 24 VDC regulated industrial PSU
* DIN-mounted terminal blocks, grounding bar, wire duct
* Aluminum backplate, labeled rail sections, ethernet switch

## 4) Networking (Training Lab)

* **Rockwell cell:** EtherNet/IP between ControlLogix, 5069-AENTR, PanelView 5310
* **Siemens cell:** PROFINET between S7-1500 CPU and ET 200 (incl. IO-Link master)

This package exists to provide a **hardware-level reference** for students, instructors, and lab techs.

---

## ✅ **Repository Structure**

```
00_Overview_Standards/   → Scope, revision log, drawing/tagging rules  
01_Mechanical_CAD/       → Panel layout, device placement, DIN rail, dimensions  
02_Electrical_Schematics/→ Power wiring, single-line diagram, terminal mapping  
03_PLC_Software/         → Controller configuration, slot layout, physical I/O table  
04_HMI_SCADA/            → PanelView model info, firmware, network config  
05_Networks_Data/        → IP addresses, Ethernet topology  
06_Testing_Commissioning/→ Power checks, comms checks, basic startup verification  
07_Ops_Maintenance/      → Power-up/power-down steps, part numbers  
08_Appendices/           → Device datasheets, manuals  
_assets/                 → Photos of Statio
_templates/              → Blank forms (tags, IO table)
```

---

## **What *is* Documented**

* Physical layout of all hardware on the station
* Catalog numbers, series, firmware (when identified)
* Slot-by-slot module configuration
* Power supply wiring and voltage distribution
* Ethernet wiring and network addresses
* PanelView hardware information & communication settings
* Terminal block numbering and layout
* Basic verification (power on, comms OK, modules healthy)

---

## **What is *NOT* Included**

* No machine sequence
* No pre-built ladder logic
* No alarms
* No operator screens
* No field inputs or outputs (none are wired)
* No process description
* No system behavior (station is a blank training platform)

---

## **Current Status**

* Repository structure created
* Initial BOM in progress
* Station photos pending upload
* Slot layout, IP plan, and wiring details to be captured in lab

---

## ✅ **Goal**

Provide a clear, accurate, professional documentation package that describes **GTCC Mechatronics PLC Lab Station**, how it is wired, and how it is configured and networked to other systems (FANUC Robots, VFDs, etc.)

---

