# sBSE

A complete set of stage-wise source codes and a representative Cy7 monomer stochastic Bethe-Salpeter Equation (sBSE) calculation accompanying the manuscript, **“Nonuniform Screening Reshapes Collective Excitons in Molecular Aggregates from Stochastic Bethe-Salpeter Theory.”**

**Contributors:** Barry Y. Li, Chern Chuang, Tim Duong, Tucker Allen, Justin R. Caram, and Daniel Neuhauser

## Repository contents

- The complete five-stage source code is provided in `/main/five_stage_srcs.zip`.
- A complete representative Cy7 monomer calculation, including input and output files, is provided in `/main/cy7_monomer_example.zip`.
- A general tutorial demonstrating compilation and execution of the code is available here:  
  https://www.youtube.com/watch?v=AOwg3HVnT04

## System requirements

### Software dependencies and operating system

- Linux/Unix-based operating system.
- MPI-enabled Fortran compiler, such as `mpif90`.
- **LIBXC 5.2.3**.

The code has been tested in Linux-based HPC environments using an MPI-enabled Fortran compiler and LIBXC 5.2.3. The implementation does not depend on a specific Linux distribution or MPI implementation.

### Hardware requirements

No GPU or other specialized accelerator hardware is required.

The code is designed for parallel CPU execution. Small systems may be run with relatively modest computational resources, whereas the large aggregate calculations reported in the manuscript require multi-core HPC resources.

## Installation

The software consists of several Fortran programs corresponding to different stages of the sBSE workflow.

1. Install an MPI-enabled Fortran compiler, such as `mpif90`.
2. Install **LIBXC 5.2.3**.
3. Extract `/main/five_stage_srcs.zip`.
4. Compile the Fortran source codes for each stage using the MPI-enabled Fortran compiler and link against LIBXC 5.2.3.

Once the compiler and LIBXC are available, compilation of the stage-wise source codes typically requires only a few minutes.

A general tutorial demonstrating compilation and execution is available at:

https://www.youtube.com/watch?v=AOwg3HVnT04

## Demo

A complete representative Cy7 monomer sBSE calculation is provided in:

`/main/cy7_monomer_example.zip`

The archive contains the input files and corresponding output files for the different stages of the calculation.

### Running the demo

1. Extract `/main/five_stage_srcs.zip`.
2. Compile the required Fortran programs as described above.
3. Extract `/main/cy7_monomer_example.zip`.
4. Enter the corresponding directory for each computational stage.
5. Run the stages sequentially using the supplied Cy7 monomer input files.
6. Compare the generated files with the supplied reference output files.

The supplied outputs show the expected results from the representative calculation and may be used to verify successful execution of each stage.

### Expected runtime

Runtime depends strongly on the number of MPI processes and the CPU resources available.

The supplied Cy7 monomer example is intended primarily for execution in a parallel Linux/HPC environment rather than on a standard desktop computer. Therefore, a meaningful desktop runtime is not specified. Compilation itself normally requires only a few minutes, while the computational runtime varies with the number of processors used.

## Instructions for use

The sBSE calculation proceeds through five computational stages. The corresponding source codes are provided in:

`/main/five_stage_srcs.zip`

The Cy7 monomer example demonstrates the directory structure, input files, output files, and stage-wise workflow used in the manuscript.

To apply the software to another molecular system, users should prepare the corresponding molecular, orbital, grid, and calculation inputs required by each stage and then follow the same sequential workflow demonstrated by the supplied example.

Production calculations for large molecular aggregates are computationally demanding and are intended for parallel CPU-based HPC systems.

## Reproducibility

The repository provides:

1. The complete stage-wise source code used for the calculations.
2. The required external dependency and version, LIBXC 5.2.3.
3. Compilation and execution instructions.
4. A complete representative Cy7 monomer calculation.
5. Input files and corresponding reference outputs for the representative calculation.
6. Instructions for executing and verifying the representative workflow.
7. A general video tutorial demonstrating compilation and execution.

The same computational workflow is used for the larger aggregate calculations reported in the manuscript.

Detailed descriptions of the theoretical formulation, numerical implementation, and computational workflow are provided in the **Methods** section and **Supplementary Information** of the accompanying manuscript.

## Source code repository

https://github.com/barryyangtao/sBSE

## License

This software is distributed under the BSD 3-Clause License. See the `LICENSE` file for details.

