# Instrumentation and Sensor Analysis

This repository contains simulations and analysis of various sensors, including LM35, TSL251, CNY70, GP2D12, and load cells. It explores their characteristics, accuracy, and applications through MATLAB curve fitting, Proteus simulations, and error calculations. A comprehensive resource for understanding and applying sensor technologies in practical instrumentation projects.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Questions Overview](#questions-overview)
  - [Question 1: LM35 Temperature Sensor](#question-1-lm35-temperature-sensor)
  - [Question 2: TSL251 Light Sensor](#question-2-tsl251-light-sensor)
  - [Question 3: CNY70 Reflective Optical Sensor](#question-3-cny70-reflective-optical-sensor)
  - [Question 4: GP2D12 Distance Sensor](#question-4-gp2d12-distance-sensor)
  - [Question 5: Load Cell for Weight Measurement](#question-5-load-cell-for-weight-measurement)
  - [Question 6: Motor Encoder](#question-6-motor-encoder)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project explores six different sensor systems, analyzing their performance and applications through simulations and theoretical calculations. Each question focuses on a specific sensor, detailing its sensitivity, range, accuracy, and usage. MATLAB and Proteus tools are used for simulation and curve fitting, while Python and C are employed for coding implementations.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/instrumentation-sensor-analysis.git
   cd instrumentation-sensor-analysis
   ```
2. **Install Required Tools**:
   - MATLAB for curve fitting and analysis.
   - Proteus for sensor simulations.
   - Python or C compilers for implementing equations.
3. **Explore Individual Questions**:
   Each question has its own directory with relevant files and scripts.

## Questions Overview

### Question 1: LM35 Temperature Sensor
- **Objective**: Analyze the LM35 sensor's sensitivity (10 mV/°C), accuracy (±0.5°C), and range (−55°C to 150°C).
- **Simulation**: Proteus simulation to verify the sensor's output at specific temperatures.
- **Key Equation**:
  ```
  θ = (Value_detected - 819.2) / 500
  ```
- **Error Analysis**: Calculates error based on ADC resolution and theoretical accuracy.

### Question 2: TSL251 Light Sensor
- **Objective**: Study the light sensor's scale factor (137 mV/(μW/cm²)) and accuracy.
- **Simulation**: Sensitivity adjustments and output verification using Proteus.
- **Key Equation**:
  ```
  signal = (DigitalValue * 3.3) * 100
  signal_desired = signal * (2/3)
  ```
- **Error Analysis**: Evaluates accuracy within ±0.7 lux.

### Question 3: CNY70 Reflective Optical Sensor
- **Objective**: Map output voltage to distance using experimental data.
- **Simulation**: MATLAB curve fitting for generating a functional equation.
- **Key Equation**:
  ```
  signal = 0.6 * (DigitalValue^2.3) - 0.34
  ```
- **Error Analysis**: Provides accuracy within ±0.01 mm.

### Question 4: GP2D12 Distance Sensor
- **Objective**: Relate output voltage to distance with high precision.
- **Simulation**: MATLAB curve fitting and Proteus simulations.
- **Key Equation**:
  ```
  signal_desired = 29 * (signal - 1.14) - 1.02
  ```
- **Error Analysis**: Accuracy within ±0.02 cm.

### Question 5: Load Cell for Weight Measurement
- **Objective**: Evaluate load cell performance for weights up to 100 kg.
- **Simulation**: Amplification and scaling using AD623 and MATLAB.
- **Key Equation**:
  ```
  signal_desired = 40 * signal - 0.2
  ```
- **Error Analysis**: Accuracy within ±0.1 kg.

### Question 6: Motor Encoder
- **Objective**: Analyze motor encoder pulses, speed, and angular measurements.
- **Simulation**: Connection to motor and pulse monitoring in Proteus.
- **Key Equations**:
  - **Speed**:
    ```
    RPM = (frequency * 60.0) / 287.0
    ```
  - **Angle**:
    ```
    Measurement_x1 * 365.0 / 287.0
    ```
- **Error Analysis**: Accuracy improves with increased interrupt counts.

## Contributing

Contributions are welcome! Please fork this repository, make changes, and submit a pull request.