# LT2326 Assignment 1

Python notebooks for multilingual tokenization and Transformer language-model experiments using English, Turkish, and Chinese.

## Requirements

Run on the course GPU server (`mltgpu` or `mltgpu-2`) with Python, PyTorch (CUDA), SentencePiece, and Matplotlib. Course data must be available at `/srv/data/lt2326-h26/a1/`.

Open notebooks with the working directory set to `notebooks/`; the code uses `Path.cwd().parent` to locate the repository root.

## Reproduce the experiments

Run these notebooks **in order**:

1. `notebooks/01_baseline_character_tokenizer.ipynb` — build and save the character tokenizer.
2. `notebooks/02_bpe_tokenizers.ipynb` — train and save the BPE tokenizers.
3. `notebooks/03_transformer_language_models.ipynb` — train the three models and save weights, parameter counts, histories, and learning curves.
4. `notebooks/04_model_evaluation.ipynb` — load trained models and produce test BPC, vocabulary-allocation, and sentence-analysis results.

To **evaluate without retraining**, run Notebook 04 using the tokenizer files in `models/tokenizers/` and the `*_weights.pt` files in `models/language_models/`.

Generated results are saved in `models/language_models/`, including `parameter_counts.json`, `training_histories.json`, `learning_curves.png`, `test_bpc_results.json`, `overall_bpc_results.json`, `vocabulary_allocation.json`, and `sentence_analysis.json`.
