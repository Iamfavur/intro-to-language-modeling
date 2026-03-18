# Intro to Language Modeling

This project is a hands-on introduction to **character-level language modeling**, using a list of names as training data.  
The central learning resource is **[main.ipynb](main.ipynb)**, which walks through the full workflow step by step.

---

## Project Focus (Read This First)

The core of this repository is the notebook:

- **[main.ipynb](main.ipynb)** → primary tutorial and implementation
- **[names.txt](names.txt)** → raw training corpus used by the notebook

If you only open one file, open **[main.ipynb](main.ipynb)**.

---

## What `main.ipynb` Covers

`main.ipynb` is designed as a progressive tutorial. It typically covers:

1. **Problem setup**
   - What language modeling is
   - Why character-level modeling is useful for names

2. **Data loading and inspection**
   - Reading the corpus from [names.txt](names.txt)
   - Inspecting dataset size, examples, and character distribution

3. **Tokenization at character level**
   - Building character vocabulary
   - Converting characters to integer IDs and back

4. **Training example construction**
   - Creating context/target pairs from names
   - Understanding next-character prediction

5. **Modeling approach**
   - Starting from simple statistical baselines (e.g., frequency-based transitions)
   - Moving toward trainable neural approaches for better generation quality

6. **Training loop**
   - Forward pass and loss computation
   - Gradient-based optimization
   - Monitoring learning behavior

7. **Sampling / generation**
   - Generating new names from the trained model
   - Comparing generated outputs with real examples

8. **Analysis and interpretation**
   - Why outputs look realistic or unrealistic
   - How model choices affect generation quality

---

## Recommended Notebook Workflow

To get the most value from [main.ipynb](main.ipynb):

1. Run cells **top to bottom** in order.
2. Do not skip preprocessing/tokenization cells.
3. Re-run generation cells multiple times to inspect diversity.
4. Change key hyperparameters (context size, embedding/hidden size, learning rate, epochs) and compare outputs.
5. Keep notes in markdown cells for observations.

---

## Repository Structure

- [main.ipynb](main.ipynb): main instructional notebook and experiments
- [names.txt](names.txt): newline-separated names dataset
- [README.md](README.md): project documentation

---

## Environment Setup (macOS + VS Code)

### 1) Create and activate a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2) Install common notebook dependencies
```bash
pip install --upgrade pip
pip install jupyter notebook numpy matplotlib torch
```

### 3) Open notebook in VS Code
- Open this folder in VS Code.
- Open [main.ipynb](main.ipynb).
- Select the `.venv` Python interpreter when prompted.
- Run all cells.

---

## Learning Outcomes

After completing [main.ipynb](main.ipynb), you should be able to:

- Explain the basics of character-level language modeling
- Build a character vocabulary and encode/decode text
- Train a simple next-character predictor
- Generate synthetic names from a learned model
- Diagnose basic modeling and sampling issues

---

## Dataset Note

The model is trained on names from [names.txt](names.txt).  
Outputs are synthetic and may resemble real names due to training data patterns.

---

## Next Steps

After finishing [main.ipynb](main.ipynb), possible extensions include:

- Add train/validation split and track validation loss
- Try different context lengths
- Compare bigram vs neural model outputs
- Introduce temperature-based sampling controls
- Save/load trained model checkpoints

---

## Quick Start

If you are starting now:

1. Open [main.ipynb](main.ipynb)
2. Run all cells
3. Generate sample names
4. Modify one hyperparameter and rerun generation
5. Record what changed