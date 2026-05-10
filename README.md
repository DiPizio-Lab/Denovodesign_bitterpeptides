# De novo design of bitter petides workflow

A computational workflow for generating artificial peptides using ZymCTRL and predicting their bitterness with BitterPep-GCN. Includes a KNIME workflow for sequence preparation and physicochemical analysis of the generated peptides.

## Requirements

- [KNIME Analytics Platform](https://www.knime.com/)
- Python ≥ 3.8
- [HuggingFace Transformers](https://huggingface.co/docs/transformers/installation)
- PyTorch
- A CUDA-compatible GPU is recommended for sequence generation

## Usage

### Step 1 — Prepare peptide sequences

Use the **first node** of the included KNIME workflow to convert your peptide sequences into FASTA format suitable for ZymCTRL input.

### Step 2 — Generate peptides with ZymCTRL

Follow the instructions on the [ZymCTRL HuggingFace model page](https://huggingface.co/AI4PD/ZymCTRL) to generate novel enzyme sequences. The model supports both zero-shot generation (given an EC number) and fine-tuning on custom sequence sets.

### Step 3 — Predict bitterness with BitterPep-GCN

Use [BitterPep-GCN](https://github.com/dipizio/BitterPep-GCN) to predict the bitterness of the generated peptides.

### Step 4 — Analyse physicochemical properties

Use the KNIME workflow to compute physicochemical descriptors for the generated and predicted peptides.

## Creator

**Alexandra Steuer**

## References

Srivastava, P.\*, Steuer, A.\*, Ferri, F., Nicoli, A., Schultz, K., Bej, S., Di Pizio, A.†, & Wolkenhauer, O.† (2024). Bitter peptide prediction using graph neural networks. *Journal of Cheminformatics*, 16, 111. [https://doi.org/10.1186/s13321-024-00909-x](https://doi.org/10.1186/s13321-024-00909-x)

Munsamy, G., Illanes-Vicioso, R., Funcillo, S., Nakou, I. T., Lindner, S., Ayres, G., Sheehan, L. S., Moss, S., Eckhard, U., Lorenz, P., & Ferruz, N. (2024). Conditional language models enable the efficient design of proficient enzymes. *bioRxiv*. [https://doi.org/10.1101/2024.05.03.592223](https://doi.org/10.1101/2024.05.03.592223)

## License

This project is licensed under the [MIT License](LICENSE).
