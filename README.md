# MDI Mechanic GAMESS report

This repo presents test results for the MDI interface implementation in the GAMESS code.

To view the README.md offline, it is suggested that you use grip (i.e., pip install grip).

[yaml]: <> ( prepend )
## Usage Instructions

This repo does not include a distribution of the GAMESS software package; users must acquire the source code of GAMESS seperately.
The GAMESS source code must then be copied into a `source/gamess` subdirectory within this repository.
Afterwords, the repo can be built using the `mdimechanic build` and `mdimechanic report` commands.

## Overview of steps

The following lists the basic steps required to run a MDI calculation.
MDI Mechanic will automatically test each of these steps and indicate whether each one is currently working or not.

[comment]: <> (Badges are downloaded from shields.io, i.e.:)
[comment]: <> (curl https://img.shields.io/badge/-working-success --output report/badges/-working-success.svg)

1. [![validate_engine](report/dynamic_badges/step_engine_build.svg)](mdimechanic.yml) The engine builds successfully
2. [![min_mdi](report/dynamic_badges/step_min_engine.svg)](mdimechanic.yml) The engine supports minimalistic MDI functionality
3. [![errors_correctly](report/dynamic_badges/step_unsupported.svg)](mdimechanic.yml) The engine correctly responds to unsupported MDI commands
4. [![completed_analysis](report/dynamic_badges/step_mdi_nodes.svg)](mdimechanic.yml) Full analysis of the engine's supported nodes and commands was completed

## Nodes

The graph indicates which nodes have been implemented in this engine and the connections between them.

![command](report/graphs/node-report.gv.svg)

## Commands

The following table indicates which MDI Standard commands are supported by this engine at each node.
Supported commands are indicated in green, while unsupported commands are indicated in gray.

[travis]: <> ( supported_commands )

## Acknowledgements

Badges are obtained from the ![shields.io](https://shields.io/) project.
