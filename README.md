# Exploring Chiral Limit in QCD Using Machine Learning

## Project Overview
This project explores the application of machine learning (ML) to identify and classify phases of matter, specifically focusing on SU(3) lattice gauge theory in Quantum Chromodynamics (QCD). The work builds upon and extends the methodology from the research paper *"Machine learning of explicit order parameters: From the Ising model to SU(2) lattice gauge theory"* to SU(3) configurations.

## Key Features
- **ML Model**: Correlation Probing Neural Network for interpreting decision functions.
- **Phase Classification**: Utilized supervised learning to classify confined and deconfined phases in SU(3) lattice gauge theory.
- **Order Parameter Extraction**: Reconstructed decision functions to reveal explicit mathematical expressions for the Polyakov loop.

---

## Objectives
1. Adapt methodologies from the original research paper for SU(3) lattice configurations.
2. Utilize neural networks to interpret decision functions and extract order parameters.
3. Investigate the classification of physical phases using Monte Carlo-sampled configurations.

---

## Methodology

### Neural Network Framework
- **Feed-Forward Neural Networks**:
  - Trained to classify phases of matter by associating configurations with probabilities.
  - Decision boundary identified at prediction probability \( D(S) = 0.5 \).

- **Correlation Probing Neural Networks**:
  - Introduced for decoding decision functions.
  - Architecture consists of:
    1. Localization Network: Identifies correlations in the receptive field.
    2. Averaging Layer: Aggregates outputs similar to magnetization in spin systems.
    3. Prediction Network: Maps aggregated outputs to prediction probabilities.

- **Polyakov Loop**:
  - The primary order parameter for phase classification.
  - Nonzero in the deconfined phase and zero in the confined phase.

### Lattice Configurations
- **SU(3) Gauge Theory**:
  - Configurations generated on a 4D lattice with temporal and spatial dimensions.
  - Utilized Monte Carlo sampling for configurations at varying lattice couplings.

- **Wilson Action**:
  - Governs the discretized Euclidean path integral used for simulations.

### Phase Transition Detection
- Neural networks trained on configurations for different coupling ranges:
  - Confined phase: \( \beta \in [1.0, 1.2] \).
  - Deconfined phase: \( \beta \in [3.3, 3.5] \).
- Predictions tested for intermediate coupling values to locate phase transitions.

---

## Results

### Phase Transition Detection
- Detected phase transition coupling:
  - \( \beta = 1.99 \pm 0.10 \) (using a \( 2 \times 1 \times 1 \times 1 \) network).
  - \( \beta = 1.97 \pm 0.10 \) (using a \( 2 \times 8 \times 8 \times 8 \) network).

### Decision Function Reconstruction
- Revealed the decision function for minimal networks.
- Expressed as a sigmoid function dependent on the Polyakov loop.
- Demonstrated strong correlation between latent predictions and the Polyakov loop.

---

## Visuals

### Network Architecture
![Neural Network Architecture](https://github.com/user-attachments/assets/20367d50-9f7e-4344-82ce-b8138e9b2cc9)


### Phase Transition Visualization
![Phase Transition](https://github.com/user-attachments/assets/572b7ff9-f0b8-4956-aebc-1b40bef7b507)

---

## Significance and Applications
1. **Interpretability**:
   - Provides insights into neural network decision-making.
   - Derives explicit order parameters from ML models.

2. **Applications in QCD**:
   - Investigates finite-density QCD phase diagrams.
   - Explores phenomena like pseudogap behavior in the Hubbard model.

3. **Future Directions**:
   - Test the methodology on models with sign problems.
   - Extend analysis to higher-dimensional systems.

---

## References
1. Wetzel, S. J. et al. *Machine learning of explicit order parameters: From the Ising model to SU(2) lattice gauge theory*. Physical Review B, 2017.
2. Wilson, K. G. *Confinement of quarks*. Physical Review D, 1974.
3. Polyakov, A. M. *Thermal properties of gauge fields and quark liberation*. Physics Letters B, 1978.
