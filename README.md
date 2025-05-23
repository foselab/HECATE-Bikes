# Test Case Generation for Simulink® Models: An Experience from the E-Bike Domain

This repository contains the necessary files to replicate a series of tests described in the _Test Case Generation for Simulink® Models: An Experience from the E-Bike Domain_ paper. The tests involve using the [Hecate](https://github.com/Hecate-SBST/Hecate) tool for test case generation and Simulink models to evaluate system behavior against defined requirements.

## Repository Folders

This repository contains a folder called `Replication_Package`.
The folder contains:

- two Simulink models (Buck and PWM)
- a script to run Hecate on them
- an initialization file containing model parameters.
- an Excel file containing the results of our experiments.
- a Python script performing the statistical tests between number of iterations and time, for the comparison between Uniform Random and Simulated Annealing.

## Requirements

To run the script and be able to open the Simulink models, ensure the following software is installed:

- [MATLAB](https://it.mathworks.com/products/matlab.html?requestedDomain) version R2024a or newer and the following Add-Ons:
  - Simulink
  - Simulink Test
  - Simscape Electrical (Simscape)
  - Parallel Computing Toolbox
- [Hecate](https://github.com/Hecate-SBST/Hecate) (Follow the instructions written in the tool repo)

## How to Install

In MATLAB, navigate to the Hecate repository and add the folders `src` and `staliro` to the active path. The _genpath_ function takes also the subfolders.

```matlab
addpath("src")
addpath(genpath("staliro"))
```

Then, add also the `Replication_Package` from this repository to the active path.

```matlab
addpath("Replication_Package")
```

## How to Run

After adding to the active path the necessary folders, navigate into the `Replication_Package` folder and run the following command to execute the test.

```matlab
runTest;
```

## Possible configurations

In the _runTest_ script, the user can change:

- the _Simulink Model_ changing the _modelName_ variable (_Buck_model_ or _PWM_model_)
- the _Test Sequence Scenario_ changing the _hecateOpt.sequence_scenario_ variable (6 available scenarios)
- the _Test Assessment Scenario_ changing the _hecateOpt.assessment_scenario_ variable (3 available scenarios)

When the user changes the Test Sequence Scenario or the Assessment Scenario, both must be activated from the Simulink Model by opening the _Test Sequence_ Block and the _Test Assessment_ Block and selecting the right scenario in the Tab Scenarios. The chosen scenario has a little thunderbolt icon.

## Statistical test results

`
Wilcoxon Rank Sum Test on average number of iterations
{'statistic': 0.037904902178945175, 'p_value': 0.9697635044861096, 'reject_null': False, 'effect_size': -0.11923687194166115, 'confidence_interval': (-4.8031564689160655, 3.5013173884562923)}
`

`
Wilcoxon Rank Sum Test on times
{'statistic': 0.16262867961000602, 'p_value': 0.8708108045360416, 'reject_null': False, 'effect_size': -0.24753480517182908, 'confidence_interval': (-4915.796179129435, 2388.6628457961033)}
`


## Contributors

The following authors contributed to the _Test Case Generation for Simulink® Models: An Experience from the E-Bike Domain_ paper:

- _Michael Marzella_, University of Bergamo, Italy
- _Andrea Bombarda_, University of Bergamo, Italy
- _Marcello Minervini_, University of Bergamo, Italy
- _Nunzio Marco Bisceglia_, University of Bergamo, Italy
- _Angelo Gargantini_, University of Bergamo, Italy
- _Claudio Menghi_, University of Bergamo, Italy and McMaster University, Canada
