# Drone Swarm for Spraying Fire Retardant



**Team:** Utkarsh, Vedant and Shresth 

## Abstract:
In recent years, due to increased effective dryness and rising temperatures, many reports have come in recording massive wildfires sprouting in various parts of the world. Though, the cause of these fires is debatable, the effect is as clear as day. The fires have caused heavy losses in both economics and survival. The reported reason for the uncontrollable spread lies in the mix of delay in response, underequipped personnels and limitations on proximity. This solutions caters to solving these problems. 

## Objective Overview:
- To cluster fire prone areas and situate a drone array in the most affective spread circle for the listed areas.
  - Analysis of topography done through sattelite imagery of the proposed forest cover.
  - Clustering areas with dense forest cover using k-means clustering algorithm.
- To detect and localize wildfire's core.
  - Detection of fire and smoke as whole object by real-time detection.
  - Saliency detection using region of interest extraction (fire's core).
  - Prediction and extrapolation of fire spread pattern and marking of surrounding areas as high risk.
- To optimize and manage an autonomous drone array for effective spraying of fire-retardant over forest fires suggesting varying physical factors.
  - To create autonomous pattern detection system to form a topology of drone network for the most efficient retardant spread.
  - Refactoring reignition of latent peat
  - Accounting in wind speed, direction, temperature, dryness, proximity to settlement.

## Required:
- Scout drone (with a camera attached{1024x768 expected})
- Drone array (expected 10-15)

## Definitions:
- The scout drone is defined by a singular drone (or small array) sent out to take images of the suspected fire prone areas at regular intervals.

- The drone array is defined as a 2-dimensional (3-dimensional in experimental stages) hypothetical symmetrically-phased linear array, linking drones as nodes in 2-d spatial map structure. The path signifies the interconnections among nodes as symbolic data links specifically designed, in this case to bring about maximum efficiency in reward functions later defined.

- The data links function as communication pathways among nodes to transfer sensory input and

- Proposition of using **Particle Swarm Optimization**, a population-based stoichastic optimization technique.

## Breakdown of work-phases:
