# GEMENI File Structure Rules

Based on the [skywater-pdk-libs-sky130_fd_sc_hd](https://github.com/chatelao/skywater-pdk-libs-sky130_fd_sc_hd) repository, the following file structure rules apply:

## Top-Level Directories

- `cells/`: Contains cell-specific definitions and library files.
- `models/`: Contains simulation models and User Defined Primitives (UDPs).
- `tech/`: Contains technology-specific files like technology LEF files.
- `timing/`: Contains timing information, typically in JSON format.

## Naming Conventions

### Cell Files
Cell-related files should follow the naming pattern:
`sky130_fd_sc_hd__<cell_name>.<extension>`

Example: `sky130_fd_sc_hd__and2.v`

### Directory Hierarchy

#### Cells
Each cell has its own subdirectory under `cells/`:
`cells/<cell_name>/`

Within each cell directory, files are named with the cell prefix:
- `sky130_fd_sc_hd__<cell_name>.v` (Verilog)
- `sky130_fd_sc_hd__<cell_name>.gds` (GDSII layout)
- `sky130_fd_sc_hd__<cell_name>.lef` (Library Exchange Format)
- `sky130_fd_sc_hd__<cell_name>.spice` (SPICE netlist)
- `sky130_fd_sc_hd__<cell_name>.json` (Cell metadata)

#### Models
Model files often follow the pattern:
`udp_<primitive_name>...`

#### Timing
Timing files are stored in the `timing/` directory and typically use the JSON format:
`sky130_fd_sc_hd__<corner>.lib.json`
