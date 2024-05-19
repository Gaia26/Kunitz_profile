# README

## HMM_model_Structures

This repository contains all files and scripts necessary for constructing a profile Hidden Markov Model (HMM) based on 3D structural alignments for the Kunitz-type protease inhibitor domain. The repository is organized into several folders, each serving a specific purpose in the model building and validation process.

## Folder Structure

- **scripts**: Contains all scripts required to run the program.
- **performance**: Stores output files and visualizations from the 5-fold cross-validation (CV) performed.
- **validation**: Holds intermediate files that are outputs of the 5-fold CV and are necessary to generate the plots and results found in the performance folder.
- **sequences**: Includes the initial datasets of proteins from the Protein Data Bank (PDB) and the output files from 3D alignments and HMM construction.

## Folder Details

### scripts
This folder includes all necessary scripts to preprocess data, perform 3D structural alignments, build the HMM model, and validate the results. Key scripts include:

- `cross_val.sh`: it runs the 5-fold CV.
- `select_fasta.py`:
- `Performance.py`: 
- `best_mcc.py`: 

### performance
This folder contains the final output files and visualizations from the 5-fold cross-validation. It includes:

- `com_set_0123.png`, `com_set_0124.png`, `com_set_0134.png`, `com_set_0234.png`, `com_set_1234.png`:
- `com_set_0123.res`, `com_set_0124.res`, `com_set_0134.res`, `com_set_0234.res`, `com_set_1234.res`:
- `out_best.txt`:

### validation
This folder stores intermediate files generated during the 5-fold CV process. These files are essential for building the plots and results in the performance folder. Key files include:

- `set_0.txt`, `set_1.txt`, `set_2.txt`, `set_3.txt`, `set_4.txt`:
- `com_set_0123.txt`, `com_set_0124.txt`, `com_set_0134.txt`, `com_set_0234.txt`, `com_set_1234.txt`:
### sequences
This folder contains the initial datasets and processed files necessary for building the HMM model. It includes:

- `clean_kunitz_3d.ali`: Initial dataset of protein sequences from PDB.
- `cut_kunitz_3d.aln`: Output of the 3D structural alignments.
- `cut_kunitz_3d.hmm`: The constructed HMM for the Kunitz-type protease inhibitor domain.
- `rcsb_pdb_custom_report_20240414163443.csv`:
## Usage

1. **Navigate to the `scripts` folder**:
   ```sh
   cd HMM_model_Structures/scripts
   ```

2. **Run the preprocessing script**:
   ```sh
   ./preprocess.sh
   ```

3. **Perform 3D structural alignments**:
   ```sh
   ./align_structures.sh
   ```

4. **Build the HMM model**:
   ```sh
   ./build_hmm.sh
   ```

5. **Validate the model with 5-fold CV**:
   ```sh
   ./validate_model.sh
   ```

6. **Generate performance plots**:
   ```sh
   python plot_results.py
   ```

