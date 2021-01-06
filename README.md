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

1. ![step2](report/dynamic_badges/step_engine_build.svg) Validate engine build
2. ![step5](report/dynamic_badges/step_min_engine.svg) Implement minimalistic MDI functionality
3. ![step6](report/dynamic_badges/step_unsupported.svg) Correctly respond to unsupported commands
4. ![step8](report/dynamic_badges/step_mdi_nodes.svg) Continue to add support for more MDI commands

## Nodes

The graph indicates which nodes have been implemented in this engine and the connections between them.

![command](report/graphs/node-report.gv.svg)

## Commands

The following table indicates which MDI Standard commands are supported by this engine at each node.
Supported commands are indicated in green, while unsupported commands are indicated in gray.

[travis]: <> ( supported_commands )

## Acknowledgements

Badges are obtained from the ![shields.io](https://shields.io/) project.
