# GEMINI File Structure Rules

Based on the [skywater-pdk-libs-sky130_fd_sc_hd](https://github.com/chatelao/skywater-pdk-libs-sky130_fd_sc_hd) repository structure, adapted for the IHP-Open-PDK (SG13G2), the following file structure rules apply:

## Top-Level Directories

- `cells/`: Contains cell-specific definitions and library files.
- `models/`: Contains simulation models and User Defined Primitives (UDPs).
- `tech/`: Contains technology-specific files like technology LEF files.
- `timing/`: Contains timing information, typically in JSON format.

## Naming Conventions

### Cell Files
Cell-related files should follow the naming pattern (using IHP SG13G2 prefix as appropriate):
`sg13g2_stdcell_<cell_name>.<extension>`

Example: `sg13g2_stdcell_and2.v`

### Directory Hierarchy

#### Cells
Each cell has its own subdirectory under `cells/`:
`cells/<cell_name>/`

Within each cell directory, files are named with the cell prefix:
- `sg13g2_stdcell_<cell_name>.v` (Verilog)
- `sg13g2_stdcell_<cell_name>.gds` (GDSII layout)
- `sg13g2_stdcell_<cell_name>.lef` (Library Exchange Format)
- `sg13g2_stdcell_<cell_name>.spice` (SPICE netlist)
- `sg13g2_stdcell_<cell_name>.json` (Cell metadata)

#### Models
Model files often follow the pattern:
`udp_<primitive_name>...`

#### Timing
Timing files are stored in the `timing/` directory and typically use the JSON format:
`sg13g2_stdcell_<corner>.lib.json`
