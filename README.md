# Parasitic Exploitation and Topological Self-Destruction in Information Ecosystems

## Overview
This repository provides the computational framework and Monte Carlo simulation code used to mathematically evaluate the long-term thermodynamic and game-theoretic viability of parasitic sabotage—specifically, the strategic use of fabricated victimhood—within scale-free information ecosystems. The model utilizes continuous-time Stochastic Differential Equations (SDEs) and the Hamilton-Jacobi-Bellman (HJB) utility framework to formalize the transition from a short-term pooling equilibrium to a long-term separating equilibrium governed by autonomous network immune responses.

## Mathematical Framework
The simulation evaluates the systemic phase transitions of an adversarial agent utilizing a sabotage strategy ($s=1$) against a baseline of honest cooperation ($s=0$). The stochastic dynamics are defined by the following core components:

*   **Reputation Dynamics ($R_i$)**: Modeled via an exponential decay penalty ($\kappa$) triggered by a Poisson detection process with intensity $\rho$, counterbalanced by a natural recovery rate ($\gamma$).
*   **Victimhood Score ($V_i$)**: Artificially inflated via fabricated signals, providing a transient gravitational pull ($\beta_2$) for resource-bearing network edges.
*   **HJB Expected Utility ($J$)**: Infinite horizon integration of the instantaneous payoff ($\pi(t)$), continuously discounted at rate $r$, to determine the true Nash Equilibrium.
*   **Topological Maintenance ($-c_k$)**: A fixed continuous cost representing the thermodynamic baseline for sustaining node existence within the scale-free topology.

## The 4-Phase Systemic Lifecycle
The computational ensemble processes millions of independent stochastic paths to model the four sequential phases of parasitic exploitation:

1.  **Phase 1: Illusion of Success**: The artificial inflation of the victimhood score generates a transient payoff maximization, mathematically establishing a Myopic Nash Equilibrium prior to signal detection.
2.  **Phase 2: Immune Response**: The probabilistic detection of deception triggers an information cascade within the superior cluster. The expected reputation undergoes an accelerated exponential decay.
3.  **Phase 3: Victim's Awakening & Inter-cluster Synchronization**: As the superior cluster's reputation breaches the critical synchronization threshold ($\theta_{sync} = 0.6$), the immune signal propagates across bridging edges, precipitating a bilateral structural collapse in the original host cluster.
4.  **Phase 4: Topological Death**: Absolute structural isolation occurs when reputation falls below the edge maintenance threshold ($\theta_R = 0.2$). Connection weights truncate to zero ($W_{ij} \to 0$), yielding a perpetual negative payoff rate ($-c_k$).

## Cross-Distributional Robustness (Independence from Empirical Calibration)
To verify that the structural collapse is a topological invariant rather than an artifact of parameter calibration, the simulation evaluates the phase transitions across three distinct initial probability distributions (1,000,000 trials each):
*   **Uniform**: Egalitarian baseline ($\mathbb{E}[R_0] \approx 0.9000$)
*   **Lognormal**: Skewed structural authority
*   **Pareto**: Extreme scale-free hub concentration ($\mathbb{E}[R_0] \approx 0.9750$)

The empirical integration demonstrates that exceptional initial authority provides merely a fractional temporal delay in the onset of the synchronization trigger. By the terminal evaluation point, topological death rates strictly converge above 99.6% across all distributions, proving that the inversion of the Nash Equilibrium is independent of the initial calibration of authority.

## Installation and Usage

### Dependencies
The codebase requires standard data science libraries and is optimized for Python 3.8+ environments.
*   `numpy`
*   `pandas`
*   `matplotlib`

### Execution
The simulation scripts are designed for direct execution in local environments or cloud-based platforms such as Google Colaboratory.

1.  Clone the repository:
    ```bash
    git clone [https://github.com/username/parasitic-exploitation-sde.git](https://github.com/username/parasitic-exploitation-sde.git)
    cd parasitic-exploitation-sde
    ```
2.  Execute the phase-specific simulation scripts (e.g., `run_4phase_sde.py`).
3.  The computational pipeline will automatically generate structured `.csv` datasets, high-resolution `.png` plots, and textual `.txt` evaluation logs summarizing the mathematical inequalities.
4.  Upon completion, the script automatically compresses the resulting directories into a downloadable `.zip` archive.

## Output File Structure
The execution pipeline generates deterministic subdirectories corresponding to the evaluated hypotheses:

*   **`robustness_results/`**: Datasets and differential evaluations for Phase 1 (Myopic Nash Equilibrium).
*   **`robustness_h2_results/`**: Temporal decay coordinates and isolation rates for Phase 2.
*   **`results_h3/` & `robustness_h3_results/`**: HJB Cumulative Expected Utility integrations and exact crossover coordinates for Phase 3.
*   **`4phase_simulation_results/`**: Consolidated transition matrices and temporal evolution arrays across all four phases.
    *   `Summary_4Phase_Dynamics.png`
    *   `data_4phase_Uniform.csv`
    *   `data_4phase_Lognormal.csv`
    *   `data_4phase_Pareto.csv`

## Author
**Yasuko Kawahata**
