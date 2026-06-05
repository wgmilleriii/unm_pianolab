# UNM Piano Lab Dante Audio Networking Pilot

Here's a draft project summary you could use for Michael, Martha, and Tatiana.

## Objective

Evaluate a modern networked audio solution for the UNM Piano Lab using existing digital pianos rather than replacing instruments.

The pilot will determine whether a Dante (Digital Audio Network Through Ethernet) system can provide the core functionality currently associated with traditional piano laboratory systems:
* Teacher monitoring of individual students
* Teacher broadcast to all students
* Student pairing and group assignments
* Individual headphone listening
* Future recording and software integration

The pilot will preserve the existing visualizer system and existing pianos.

## Existing Piano Inventory

| Manufacturer | Model | Quantity |
| :--- | :--- | :--- |
| **Roland** | F-110 | 4 |
| | DP-990F | 6 |
| | F-140R | 4 |
| **Yamaha** | YDP-164 | 2 |
| | YDP-163 | 3 |
| **Total** | | **19** |

## Pilot Scope

The proof-of-concept will include:
* **1 Teacher Station**
* **3 Student Stations**
* **Total: 4 networked stations**

This configuration allows testing of:

* **Monitoring**: Teacher listens to any student.
* **Broadcast**: Teacher sends audio to all students.
* **Pairing**:
    * Student 1 paired with Student 2.
    * Student 3 paired with Teacher.
* **Recording**: Optional recording of student performances through Dante Virtual Soundcard.

## Proposed Architecture

Each station consists of the following signal chain:
* **Piano** → **Dante Transmitter** → **Ethernet Network**
* **Ethernet Network** → **Dante Receiver** → **Headphone Amplifier** → **Student Headphones**

Key components:
* All stations connect to a central **PoE network switch**.
* The teacher computer runs **Dante Controller** software for routing.

## Existing Systems Preserved

The existing MIDI visualizer system remains unchanged.

Teacher Piano MIDI Out → Existing Visualizer

The pilot only replaces audio routing functionality.

## Shopping List & Estimated Pilot Cost

| Item | Description | Quantity | Est. Unit Cost | Est. Total Cost |
| :--- | :--- | :--- | :--- | :--- |
| **Dante Transmitters** | ToVi / OREI Dante XLR Audio Encoder | 4 | $129 | $516 |
| **Dante Receivers** | ToVi / OREI Dante XLR Audio Decoder | 4 | $129 | $516 |
| **Headphone Amps** | HA400 Four-Channel Headphone Amplifiers | 4 | $22 | $88 |
| **Network Switch** | 24-Port Gigabit PoE Switch | 1 | $150 | $150 |
| **Cables & Adapters** | TRS/XLR breakout, XLR/TRS, Ethernet | - | - | $250 |
| **Software (Optional)**| Dante Virtual Soundcard | 1 | $50 | $50 |
| **Software** | Dante Controller | 1 | Free | $0 |
| **Total** | | | | **~$1,570** |

**Expected pilot budget range:** $1,500–1,800

## Benefits
* **Cost-Effective**: Retains all 19 existing pianos and avoids $25k–35k replacement costs.
* **Standardized**: Uses standard Ethernet networking (PoE).
* **Flexible**: Expandable and vendor-neutral.
* **Future-Proof**: Supports future recording and software integration.
* **Non-Disruptive**: Preserves the existing MIDI visualizer system.
* **Low-Risk**: Provides a small-scale evaluation before full deployment.

## Success Criteria
The pilot will be considered successful if it demonstrates:
* Reliable **low-latency** audio transmission.
* Functional **Teacher monitoring** of any student station.
* Functional **Teacher broadcast** to all student stations.
* Successful **Student pairing** and grouping functionality.
* **High audio quality** suitable for piano instruction.
* **Ease of operation** for instructors.

> [!TIP]
> **Recommendation**: Before purchasing all four stations, buy one transmitter, one receiver, and one headphone amp to verify audio quality and latency with a Roland F-140R. This ~$300 initial experiment will confirm the hardware choice before committing the full pilot budget.
