# sBSE

A complete set of stage-wise source codes and a representative Cy7 monomer stochastic Bethe-Salpeter Equation (sBSE) calculation accompanying the manuscript, **“Nonuniform Screening Reshapes Collective Excitons in Molecular Aggregates from Stochastic Bethe-Salpeter Theory.”**

**Contributors:** Barry Y. Li, Chern Chuang, Tim Duong, Tucker Allen, Justin R. Caram, and Daniel Neuhauser

## Repository contents

- The complete five-stage source code is provided in `/metadata/five_stage_srcs.zip`.
- A complete representative Cy7 monomer calculation, including input and output files, is provided in `/metadata/cy7_monomer_example.zip`.
- A general tutorial demonstrating compilation and execution of the code is available here:  
  https://www.youtube.com/watch?v=AOwg3HVnT04

## System requirements

- Linux/Unix-based environment.
- MPI-enabled Fortran compiler, such as `mpif90`.
- LIBXC 5.2.3.
- No GPU or other specialized accelerator hardware is required.
- Production calculations are designed for parallel CPU-based HPC systems.

## Installation

The code consists of several Fortran programs corresponding to different stages of the sBSE workflow. Each stage is compiled separately using an MPI-enabled Fortran compiler and linked against LIBXC 5.2.3.

The source files required for all five stages are included in:

`/metadata/five_stage_srcs.zip`

A general compilation and execution tutorial is available at:

https://www.youtube.com/watch?v=AOwg3HVnT04

Once the required compiler and LIBXC are available, compilation itself is typically short. The code is primarily intended for Linux-based HPC environments rather than single-workstation execution.

## Demo calculation

A complete representative Cy7 monomer sBSE calculation is provided in:

`/metadata/cy7_monomer_example.zip`

The archive contains the input files and corresponding outputs for the different stages of the calculation. These files provide a representative example of the workflow used in the manuscript.

The same stage-wise procedure is used for the larger aggregate calculations reported in the paper.

## Instructions for use

The sBSE workflow proceeds through five computational stages. The corresponding source codes are provided in `/metadata/five_stage_srcs.zip`.

Users may adapt the supplied Cy7 monomer example to their own molecular systems by replacing the relevant molecular, grid, and calculation input files while retaining the same stage-wise workflow.

Because the production calculations reported in the manuscript involve large molecular aggregates and substantial parallel CPU resources, they are intended to be run on HPC systems rather than on a standard desktop computer.

## Reproducibility

The repository provides:

1. The complete source code used in the calculations.
2. The required external dependency and version.
3. A complete representative Cy7 monomer calculation.
4. Input and output files for the representative run.
5. A general compilation and execution tutorial.

The detailed theoretical formulation and computational workflow are described in the Methods section and Supplementary Information of the accompanying manuscript.
