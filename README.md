# TUM EDGAR: Digital Twin

Welcome to the EDGAR Digital Twin repository of the Technical University of Munich! Here you find data, parameters, and information related to our TUM EDGAR research vehicle.

![EDGAR](source/docs/EDGAR_Digital_Twin.png)


## What is a Digital Twin?

A digital twin is a virtual representation of a physical object or system. In the case of our repository, the digital twin serves as a digital counterpart of our autonomous research vehicle. It captures the vehicle's behavior, performance, and characteristics in a virtual environment. With this information you can simulate the EDGAR vehicle in various 2D and 3D simulation environments.

## Repository Content

This repository is organized into the two sections of `source` and `tools`. `source` contains all parameters and models of the vehicle. `tools` contains tools to integrate the digital twin in dedicated development environments.

### Source


#### 3D Model

We provide a 3D model for the autonomous research vehicle body. This model can be integrated into 3D simulations, allowing you to visualize the vehicle and its sensors.
The 3D model files can be found in the folder `3d_model`. We offer a `high_res` and a `low_res` version of the 3D-model for various use cases. See the READMEs in the folders for more details.

#### Sensor Parameters

In this folder, we provide a detailed parameter set that specifies the position (x, y, z) of the sensors in relation to the rear axle (base link) of the autonomous research vehicle.
The `x`, `y`, and `z` values represent the coordinates in meters, indicating the displacement of each sensor from base link along the respective axes.
The parameter set can be found in the file [edgar.urdf](source/sensor_parameter/edgar.urdf) located in the `sensor_parameter` directory. We refer to the [README](source/sensor_parameter/README.md) for further details.


#### Vehicle Dynamics Parameters

We provide a list of parameters that define the vehicle dynamics of our autonomous research vehicle. These parameters can be utilized in various vehicle dynamic models, enabling accurate simulation and analysis of the vehicle's behavior.
The parameter set can be found in the file [vehicle_parameters_edgar.yaml](source/vehicle_dynamics_parameter/vehicle_parameters_edgar.yaml) file located in the `vehicle_dynamics_parameter` directory. Each parameter is listed with its corresponding value and its unit.

<!-- ### Network Parameters -->

### Tools


#### AWSIM
The given tool can be used to integrate our research vehicle as 3D-model in the [AWSIM](https://github.com/tier4/AWSIM) simulation environment by TierIV. A detailed description how to use the tool is given in the [README](tools/AWSIM/README.md).

#### Edgar State Publisher
By means of the given guide, EDGAR can be visualized in the Robot State Publisher based on the given .urdf-file. A detailed description how to use the tool is given in the [README](tools/edgar_state_publisher/README.md).


<!-- #### CARLA -->


## Contact

If you have any questions, feel free to contact our [EDGAR-Team](https://www.mos.ed.tum.de/en/ftm/main-research/intelligent-vehicle-systems/edgar/).

## References
P. Karle et al., "EDGAR: An Autonomous Driving Research Platform - From Feature Development to Real-World Application" (under review)

<!-- BibTex:
```
@ARTICLE{Karle2023_2,
  author={Karle, Phillip and Török, Ferenc and Geisslinger, Maximilian and Lienkamp, Markus},
  journal={IEEE Access},
  title={MixNet: Physics Constrained Deep Neural Motion Prediction for Autonomous Racing},
  year={2023},
  volume={11},
  number={},
  pages={85914-85926},
  doi={10.1109/ACCESS.2023.3303841}
}
``` -->
