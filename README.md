# Folded-Cascode CMOS Operational Amplifier

## Overview

This project presents the design and simulation of a **folded-cascode CMOS operational amplifier** using **Cadence Virtuoso** and **GPDK 180 nm** technology.

The folded-cascode architecture uses a folded structure to route current from the input differential pair to the cascode load. This architecture provides **high voltage gain** and improved output swing compared with a telescopic architecture, while remaining suitable for low-voltage and high-speed applications.

## Objectives

* Design a folded-cascode CMOS operational amplifier.
* Analyze the frequency response and dynamic performance.
* Evaluate gain, CMRR, slew rate, UGB, THD, phase margin, bandwidth, power consumption, and noise.
* Study the effect of device mismatch using Monte Carlo analysis.
* Evaluate circuit robustness using PVT analysis.
* Analyze the major noise sources in the circuit.

## Tools and Technology

| Parameter    | Details                     |
| ------------ | --------------------------- |
| EDA Tool     | Cadence Virtuoso            |
| Technology   | GPDK 180 nm                 |
| Circuit      | Folded-Cascode CMOS Op-Amp  |
| Architecture | Single-stage folded-cascode |
| Analyses     | AC, Noise, Monte Carlo, PVT |

## Circuit Architecture

The folded-cascode amplifier uses a **folded structure** to transfer current from the input differential pair to the cascode load.

Compared with a telescopic architecture, the folded structure provides improved output swing while maintaining high gain.

The architecture requires careful biasing to ensure that all MOSFETs remain in the **saturation region** during operation.

### Key Features

* High voltage gain
* Improved output swing compared with telescopic architecture
* Low-power operation
* High-speed operation
* Suitable for low-voltage analog applications
* Requires multiple bias voltages and careful biasing

## Schematic

![Folded-Cascode Op-Amp Schematic](schematic.png)

## AC Analysis

AC analysis was performed to characterize the small-signal frequency response of the folded-cascode amplifier.

The analysis evaluates voltage gain, CMRR, slew rate, unity-gain bandwidth, THD, phase margin, bandwidth, power consumption, and noise.

![AC Analysis](ac_analysis.png)

### Nominal AC Performance

| Parameter            |             Result |
| -------------------- | -----------------: |
| Gain                 |           89.36 dB |
| CMRR                 |         114.168 dB |
| Slew Rate            |          4.79 MV/s |
| Unity-Gain Bandwidth |          9.766 MHz |
| THD                  |             0.366% |
| Phase Margin         |             81.20° |
| Power Consumption    |           12.89 µW |
| Bandwidth            |         332.615 Hz |
| Noise                | 5.27 × 10⁻¹⁷ V/√Hz |

## Monte Carlo Analysis

Monte Carlo analysis was performed to evaluate the effect of statistical device mismatch on the performance of the folded-cascode amplifier.

The simulation results showed stable frequency response and low-power operation with variations in the circuit parameters.

### Monte Carlo Mean Results

| Parameter            | Mean Value |
| -------------------- | ---------: |
| Unity-Gain Bandwidth |   8.65 MHz |
| Power Consumption    |    33.7 µW |
| Slew Rate            |  48.1 MV/s |
| Phase Margin         |      87.1° |
| CMRR                 |    56.8 dB |

The phase margin remained high, indicating good stability across the simulated mismatch conditions.

![Monte Carlo Analysis](monte_carlo.png)

## Noise Analysis

Noise analysis was performed to identify the dominant noise mechanisms in the folded-cascode architecture.

The major noise sources include:

* Input differential pair
* Current mirrors
* Bias branches

### Noise Behavior

At low frequencies, **flicker noise (1/f noise)** is the dominant noise mechanism.

At higher frequencies, **thermal noise** becomes the dominant contributor.

The folded-cascode architecture contains more noise paths than a telescopic amplifier because of its folded signal path and additional biasing branches.

![Noise Analysis](noise_analysis.png)

## PVT Analysis

PVT analysis was performed to evaluate circuit behavior under process, voltage, and temperature variations.

The analysis provides insight into the robustness of the folded-cascode amplifier under different operating conditions.

### PVT Observations

| Parameter         | Observed Value |
| ----------------- | -------------: |
| Power Consumption |       ~33.7 µW |
| Slew Rate         |     ~47.9 MV/s |
| Bandwidth         |       ~336 kHz |
| CMRR              |         ~85 dB |

![PVT Analysis](pvt_analysis.png)

## Performance Summary

### Nominal Performance

| Parameter    |     Result |
| ------------ | ---------: |
| Gain         |   89.36 dB |
| CMRR         | 114.168 dB |
| UGB          |  9.766 MHz |
| Slew Rate    |  4.79 MV/s |
| THD          |     0.366% |
| Phase Margin |     81.20° |
| Power        |   12.89 µW |
| Bandwidth    | 332.615 Hz |

### Robustness Analysis

The Monte Carlo and PVT simulations were used to evaluate the effect of mismatch and operating-condition variations.

The results demonstrate:

* High phase margin
* Low-power operation
* Stable unity-gain bandwidth
* Good common-mode rejection
* Fast slew response

## Key Design Trade-offs

| Parameter       | Folded-Cascode Architecture                  |
| --------------- | -------------------------------------------- |
| Gain            | High                                         |
| Output Swing    | Better than telescopic                       |
| Power           | Low                                          |
| Speed           | High                                         |
| Noise           | Multiple noise paths                         |
| Biasing         | More complex                                 |
| Main Advantage  | High gain with improved output swing         |
| Main Limitation | Increased circuit complexity and noise paths |

## Key Design Concepts

This project provided practical experience with:

* Folded-cascode amplifier architecture
* CMOS differential pair design
* Cascode structures
* Current mirrors
* Bias voltage generation
* High-output-impedance design
* Gain enhancement through cascoding
* Frequency-response analysis
* Noise analysis
* Monte Carlo mismatch analysis
* PVT analysis
* Phase-margin and stability evaluation
* Low-power analog circuit design

## Conclusion

A **folded-cascode CMOS operational amplifier** was designed and simulated using **Cadence Virtuoso with GPDK 180 nm technology**.

The design achieved a nominal voltage gain of **89.36 dB**, unity-gain bandwidth of **9.766 MHz**, phase margin of **81.20°**, and power consumption of **12.89 µW**.

Monte Carlo and PVT analyses were performed to study circuit robustness under mismatch and operating-condition variations. Noise analysis showed that flicker noise dominates at low frequencies while thermal noise becomes dominant at higher frequencies.

The project demonstrates the practical trade-offs between **gain, output swing, speed, power consumption, noise, and biasing complexity** in folded-cascode analog amplifier design.
