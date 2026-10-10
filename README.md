# Learning Recommender Systems

Notebooks and explanations for learning recommender systems through hands-on experiments. Each topic has its own section below with the relevant notebook, concepts, and experiments to try. The notebooks are exploratory work in progress you can run and extend.

## Topics

| Topic | Notebook |
| --- | --- |
| [Vector quantization](#vector-quantization) | [vector_quantization.ipynb](vector_quantization.ipynb) |

## Run locally

Run these commands from the repository root:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
jupyter lab
```

For topics using MovieLens, follow [datasets/README.md](datasets/README.md) to place the data locally. Open notebooks from this folder so relative data paths resolve correctly. Dependencies are unpinned starting requirements, not a verified environment lockfile.

## Vector quantization

**Notebook:** [vector_quantization.ipynb](vector_quantization.ipynb)

Vector quantization represents continuous vectors using a finite set of learned codebook vectors. This notebook applies it to movie embeddings learned by a recommendation model, then explores the movies assigned to each code.

### Walkthrough

Start with basic familiarity with Python, pandas, and PyTorch tensors. Run the cells in order from a fresh kernel:

1. Load MovieLens ratings and movie metadata, then prepare training and validation data.
2. Train a model using user and movie embeddings with an MLP to predict ratings.
3. Extract the learned movie embeddings and train a vector quantization codebook.
4. Inspect the movies and genres assigned to each code to explore what the groups capture.

### Experiments to try

- Add a mean-rating baseline to put the model's prediction error in context.
- Change the embedding dimension and compare validation results.
- Change the codebook size and compare quantization error and code usage.
- Inspect whether movies assigned to the same code share genres.

## Recording experiments

Use [EXPERIMENTS.md](EXPERIMENTS.md) to record settings, metrics, and conclusions across topics. Keep the data split consistent when comparing models, and record the random seed so results are easier to reproduce.

Raw data and model files stay local; notebooks, notes, and recorded results belong in Git.
