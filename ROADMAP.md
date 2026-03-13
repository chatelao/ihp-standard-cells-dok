# IHP-Open-PDK Documentation Roadmap

This roadmap outlines the tasks required to achieve a documentation quality comparable to the SkyWater SKY130 PDK.

## Phase 1: Infrastructure and Process

### 1. Documentation Infrastructure Setup
- [ ] Configure Sphinx with Material theme for a modern look and feel.
- [ ] Set up automated builds and hosting on ReadTheDocs.
- [ ] Define a clear directory structure for RST/Markdown source files.
- [ ] Implement search and indexing features.

### 2. Process Specification Documentation
- [ ] Provide a detailed overview of the SG13G2 130nm BiCMOS process.
- [ ] Create a Process Stack Diagram showing layers and thicknesses.
- [ ] Document semiconductor criteria, junction depths, and implant angles.

### 3. Layer Definitions and Reference
- [ ] Create a comprehensive GDSII layer mapping table.
- [ ] Define auxiliary layers and their specific purposes in the design flow.
- [ ] Document device-to-layer associations for LVS (Layout vs. Schematic).

### 4. Physical Design Rules (DRC)
- [ ] Document periphery rules for all metal and poly layers.
- [ ] Categorize rules by type: Width, Spacing, Enclosure, and Extension.
- [ ] Provide visual diagrams for complex or non-obvious design rules.

### 5. Mask and Manufacturing Criteria
- [ ] Document mask-specific assumptions and manufacturing constraints.
- [ ] Define minimum critical dimensions for all critical layers.
- [ ] Specify latch-up prevention and ESD design criteria.

## Phase 2: Device and Library Details

### 6. Device Details: Spice Models
- [ ] Document models for 1.2V and 3.3V NMOS/PMOS transistors.
- [ ] Provide detailed parameter documentation for SiGe:C HBTs.
- [ ] Document passive device models including resistors, capacitors, and varactors.

### 7. Device Details: Layout and Symbols
- [ ] Generate and document primitive device symbols for Xschem and Qucs-S.
- [ ] Provide representative layout examples for each primitive device.
- [ ] Document device-specific DRC/LVS caveats or special handlings.

### 8. Standard Cell Library: General Info
- [ ] Document the naming convention used for standard cells.
- [ ] Define cell sizing strategies (e.g., drive strengths, low power variants).
- [ ] Create library-level characterization summaries (timing, power, area).

### 9. Standard Cell Library: Cell-Specific READMEs
- [ ] Create a detailed README for every cell in the library (e.g., `nand2`, `inv`).
- [ ] Define a standard template: Logic equations, Pin descriptions, and Truth tables.
- [ ] Link each cell's documentation to its Verilog, Spice, and GDSII source.

### 10. Standard Cell Library: Visual Assets
- [ ] Automate the generation of SVG symbols for all standard cells.
- [ ] Generate SVG schematics showing the internal transistor topology.
- [ ] Create SVG layout previews for quick reference in the documentation.

## Phase 3: Libraries and IP

### 11. IO and Periphery Library Documentation
- [ ] Document ESD protection schemes and pad architectures.
- [ ] List all available IO cells with their electrical specifications.
- [ ] Provide guidelines for building pad rings and power/ground distribution.

### 12. SRAM Library Documentation
- [ ] Document the architecture and bitcell details for provided SRAMs.
- [ ] Provide instructions for using SRAM compilers or configuring macros.
- [ ] List performance specifications for pre-generated SRAM blocks.

## Phase 4: Design Flows and Verification

### 13. Analog Design Flow Documentation
- [ ] Create a step-by-step tutorial for the Xschem to Magic/KLayout flow.
- [ ] Document analog layout techniques specific to the SG13G2 process.
- [ ] Provide example testbenches for common analog building blocks.

### 14. Digital Design Flow Documentation
- [ ] Document the OpenROAD-based RTL-to-GDSII flow for IHP-Open-PDK.
- [ ] Provide example synthesis and P&R constraints files.
- [ ] Include a "Hello World" digital block tutorial.

### 15. Simulation Methodology and Examples
- [ ] Document the setup and usage of Ngspice and Xyce simulators.
- [ ] Provide examples for Corner simulations (PVT).
- [ ] Document procedures for Monte Carlo and Mismatch analysis.

### 16. Physical and Design Verification (DRC/LVS/PEX)
- [ ] Document the usage of KLayout DRC/LVS decks.
- [ ] Provide instructions for running verification with Magic and Netgen.
- [ ] Create a "Tape-out Checklist" for final design validation.

### 17. Parasitic Extraction (RCX) Rules
- [ ] Document resistance and capacitance rules for all interconnect layers.
- [ ] Provide lookup tables for typical wire parasitics.
- [ ] Compare extraction results between different supported tools.

## Phase 5: Community and Maintenance

### 18. Python API Documentation
- [ ] Document any Python-based tools or APIs provided with the PDK.
- [ ] Provide scripts for automated cell analysis or PDK customization.
- [ ] Document utility functions for layout generation (e.g., PyCells).

### 19. Contributor Guidelines and Code Review
- [ ] Define the Contributor License Agreement (CLA) process.
- [ ] Document the workflow for reporting bugs and submitting pull requests.
- [ ] Set up automated linting and documentation-build checks.

### 20. Roadmap and Versioning Management
- [ ] Maintain a public Gantt chart or milestone list for PDK development.
- [ ] Document the versioning format and provide a detailed Changelog.
- [ ] Define the process for feature deprecation and process updates.
