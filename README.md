# IEEE 33-Bus Radial Distribution Network Power Flow & Loss Minimization

[![MATLAB](https://img.shields.io/badge/MATLAB-R2023b%20%7C%20R2024b-0076A8?logo=mathworks&logoColor=white)](https://www.mathworks.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Domain](https://img.shields.io/badge/Domain-Electric%20Power%20Distribution%20Systems-lightgrey.svg)](#)

A standalone MATLAB implementation of IEEE 33-Bus Radial Distribution Network Power Flow. Includes the governing dynamics, analytical formulations, and an executable script you can run directly without proprietary third-party dependencies.

## Overview

This repository provides a Backward/Forward Sweep (BFS) power flow solver tailored for radial distribution networks using the standard IEEE 33-bus feeder topology. It calculates bus voltages, branch currents, and total real power losses.

## Governing Equations & Mathematical Formulation

### Backward Current Sweep

$$
I_{k} = \left(\frac{S_{k}}{V_{k}}\right)^* + \sum_{m \in \mathcal{C}_k} I_{km}
$$

### Forward Voltage Sweep

$$
V_{m} = V_{k} - Z_{km} I_{km}
$$

where $S_k$ is the complex power demand at bus $k$, $Z_{km} = R_{km} + j X_{km}$ is the branch impedance, and $\mathcal{C}_k$ is the set of children connected to bus $k$.

## Getting Started

### Prerequisites
- MATLAB (tested on R2022b through R2024b)
- Standard base MATLAB installation (no paid external toolboxes required for this starter script)

### Running the Code
1. Clone the repository:
   ```bash
   git clone https://github.com/matlabsolutions-simulink/matpower-ieee-33-bus-optimal-power-flow.git
   cd matpower-ieee-33-bus-optimal-power-flow
   ```
2. Open MATLAB, navigate to the cloned folder, and run:
   ```matlab
   run_ieee33_bus_power_flow
   ```

## Need the Complete Simulink or Simscape Model?

If you are working on a university capstone, thesis, or lab assignment and need the complete `.slx` model with Simscape physical networks, custom parameter lookup tables, or automated test harnesses, our team at [MATLABSolutions.com](https://www.matlabsolutions.com/order-now.php?ref=github_matpower_ieee_33_bus_optimal_power_flow) provides custom academic simulation and consulting support.

## Technical Inquiries & Contact
- Website: [matlabsolutions.com](https://www.matlabsolutions.com)
- Custom Consulting Portal: [matlabsolutions.com/order-now.php](https://www.matlabsolutions.com/order-now.php)
- Email: info@matlabsolutions.com

## License
This project is open-source under the [MIT License](LICENSE).
