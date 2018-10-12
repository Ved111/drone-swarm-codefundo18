# Self-Contained Wildfire Prediction and Counteraction System 
*A project by team O(N)Cube

**Team:** Utkarsh, Vedant and Shresth 

## Abstract:
Forests and forest ecosystems are of key importance for the social, economic and environmental viability. They hold importance in economic factors and at the same time supply complex, dynamic, highly valuable natural ecosystems that also facilitate and protect
biodiversity.
The current meta of forest has seen a peaking rise in forest fires and many communities have had their fair share of losses in these recurrent phenomenon, be it economical, social, diversity or life. Many reports have come in recording massive wildfires sprouting in various parts of the world, most accounted to be the results of increasing dryness and rising temperatures. Though, the cause of these fires is debatable, the effect is as clear as day. The reported reason for the uncontrollable spread lies in the mix of delay in response, underequipped personnels and limitations on proximity. This solutions caters to solving these problems. 

The project encompasses the profiling, prediction and mitigation of wildfire spread. The project can be divided roughly into 4 phases.
- Prediction
- Prevention
- Mitigation
- Relief

### Prediction:
The proposed phenomenon is a very erratic in nature, but, certain parameters sure help in determining the severity of destruction, if not, the prediction of occurance per se. The prediction phase requires the profiling of forest cover to look for certain features topography that might contribute in fire eruption or propogation.

The factors considered are:
- Density of forest cover
- Area of continuous cover
- Tree characteristics
- Wind patterns
- Temperature patterns
- Presence of peat in soil
- Previous instances of wildfire
- Time taken to put it out
- Vicinity to human settlements
- Presence of forest chain breaks

A radial prediction mapping is expected to mark zones of wildfire occurances and their destruction pattern using the fed features. It is thus proposed to use a radial basis function classifier to map out such zones. The job of classification of the zones is provided to a Gaussian RBF Classifier Network. The features will be updated by training the model with new training data in case new wildfires occur.

### Prevention and Mitigation:
A drone hub is placed in the high risk area. This hub consists of multiple meshing drones and a scout drone. The scout drone is fitted with a basic camera.The scout drone is lifted to a high elevation point to survey the forest and look out for wildfires. The wildfires are detected using Saliency detection coupled with sliding window function optimization for more accurate shape detection.

The scout drone sends this information along with the target location to drone mesh controller. The mesh drones are a series of drones that are fitted with dumping buckets containing fire retardants. The aim is to propose a fully automated aerial fire-fighting method. To do the same, we propose using a reinforced learning model. The input info along with wind speed, temperature and other real-time parameters(later decided) are fed into a reinforcement learning model that learns and gives out two outputs:
- Number of drones required
- Proposed formation

The mesh drones are dispatched from the hub and form suitable cover over the wildfire according to the proposed topology.%%%% The retardants are then released onto the fire's core. After the operation drones are returned to the hub. If the fire still persists, the drones are sent again. During this time scout drone watches over the wildfire and creates a reward function based on the retarding speed of the fire's core. This reward function is later fed into reinforcement learning model of drone for future iterations.

### Relief(future iteration):
- Human detection
- Damage prediction
- Damage effect prediction and relief work

## Iterations:
This is a constantly evolving system, which continues to learn from each failed and successful attempt. The results are fed back into scout drone, mesh drones and prediction models.

## Objective Overview:
- To cluster fire prone areas and situate a drone array in the most affective spread circle for the listed areas.
  - Analysis of topography done through satellite imagery of the proposed forest cover.
  - Clustering areas with dense forest cover using k-means clustering algorithm.
- To detect and localize wildfire's core.
  - Detection of fire and smoke as whole object by real-time detection.
  - Saliency detection using region of interest extraction (fire's core).
  - Prediction and extrapolation of fire spread pattern and marking of surrounding areas as high risk.
- To optimize and manage an autonomous drone array for effective spraying of fire-retardant over forest fires suggesting varying physical factors.
  - To create autonomous pattern detection system to form a topology of drone network for the most efficient retardant spread.
  - Refactoring reignition of latent peat
  - Accounting in wind speed, direction, temperature, dryness, proximity to settlement.

## Definitions:
- The scout drone is defined by a singular drone (or small array) sent out to take images of the suspected fire prone areas at regular intervals.

- The drone array is defined as a 2-dimensional (3-dimensional in experimental stages) hypothetical symmetrically-phased linear array, linking drones as nodes in 2-d spatial map structure. The path signifies the interconnections among nodes as symbolic data links specifically designed, in this case to bring about maximum efficiency in reward functions later defined.

- The data links function as communication pathways among nodes to transfer sensory input and
