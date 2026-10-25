# Mini NLP Project: Transformer Encoder for Sentiment Classification

This notebook demonstrates the core building blocks of a Transformer encoder by implementing a small sentiment classifier in PyTorch.

## Project overview

The project uses a small, hand-crafted dataset of 16 short positive and negative movie-related sentences. It walks through text preprocessing and a compact Transformer encoder implementation rather than relying on a pretrained language model.

### Concepts demonstrated

- Simple whitespace tokenization
- Vocabulary construction with `<PAD>` and `<UNK>` tokens
- Conversion of words to token IDs
- Sequence padding and attention masks
- A custom PyTorch `Dataset` and `DataLoader`
- Multi-head self-attention
- Residual connections and layer normalization
- Position-wise feed-forward network
- Token and positional embeddings
- A Transformer encoder block and classification head
- Sentiment predictions and attention-weight visualization

## Model and data

- **Task:** Binary sentiment classification
- **Labels:** Positive (`1`) and negative (`0`)
- **Dataset size:** 16 example sentences
- **Architecture:** One custom Transformer encoder block
- **Framework:** PyTorch

The notebook's saved training output shows the loss falling to a very small value on this tiny dataset. This is an educational demonstration, **not evidence of generalization to real-world sentiment data**. The notebook evaluates example sentences but does not provide a held-out test-set benchmark.

## Tech stack

- Python
- PyTorch
- Matplotlib
- Jupyter Notebook

## Installation

Create and activate a virtual environment.

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

macOS/Linux:

```bash
source .venv/bin/activate
python -m pip install -r requirements.txt
```

## Run the notebook

```bash
jupyter notebook Mini_NLP_Project_Transformer_Encoder.ipynb
```

Run the cells from top to bottom. No external dataset is required; the example sentences are defined inside the notebook.

## Repository structure

```text
transformer-encoder-sentiment-classifier/
├── Mini_NLP_Project_Transformer_Encoder.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Limitations and possible extensions

- The dataset contains only 16 short examples, so the model can easily memorize it.
- Tokenization is a simple lowercase whitespace split; it does not handle subwords or punctuation robustly.
- There is no train/validation/test split in the current notebook.
- Add a larger labeled dataset, proper held-out evaluation, and metrics such as precision, recall, F1-score, and a confusion matrix before making performance claims.
- Compare against a simple baseline and consider testing padding-mask behavior carefully.
- Attention visualizations can be informative but should not automatically be interpreted as a complete explanation of the model's decisions.

## License

No license has been specified. Add a `LICENSE` file if you want to define reuse and distribution terms.
