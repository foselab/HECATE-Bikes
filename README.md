# HECATE_FSE_2025_Industry_Bikes
This repository contains the necessary files to replicate a series of tests described in the *HECATE_FSE_2025_Industry_Bikes* paper (ADD LINK/REFERENCE). The tests involve using the Hecate tool for test case generation and Simulink models to evaluate system behavior against defined requirements.

This repository contains a folder called `Replication_Package`.
The folder contains two Simulink models, a script to run Hecate on them and an initialization file containing model parameters.

## Requirements
Before running the script, ensure the following software is installed:

* MATLAB version r2022b or newer
* Simulink version compatible with MATLAB
* Hecate tool installed (Follow the instructions written in https://github.com/Hecate-SBST/Hecate)

## How to Run

The tests can be run after adding to the active path the folders from Hecate ('src' and 'staliro') and the `Replication_Package` folder.    
The following code adds to the path the `Replication_Package` folder and run the test. The 'src' and 'staliro' folder are added automatically by the script. 

```matlab
addpath("Replication_Package")
runTest;
```


# Contributors
The following authors contributed to the *HECATE_FSE_2025_Industry_Bikes* paper:

* *Michael Marzella*, University of Bergamo, Italy
* *Claudio Menghi*, University of Bergamo, Italy and McMaster University, Canada
* *Andrea Bombarda*, University of Bergamo, Italy
* *Marcello Minervini*, University of Bergamo, Italy
* *Angelo Gargantini*, University of Bergamo, Italy 
