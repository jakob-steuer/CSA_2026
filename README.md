# HPC hands-on: scaling, balancing and scheduling

A ~60-minute exercise for the lecture *High Performance Computing (HPC)* (Computer & Software Architectures, FHNW).
No cluster, no installation and no account is needed: everything runs in Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jakob-steuer/CSA_2026/blob/main/hpc_exercise.ipynb)

## What you will do

| Part | Question | Time |
|---|---|---|
| 1 | What does "running in parallel" mean, and does it always help? | 10 min |
| 2 | Why are 100 cores not 100× faster? (Amdahl's law, strong vs weak scaling) | 10 min |
| 3 | How do you share uneven work fairly? (static, round robin, dynamic) | 10 min |
| 4 | How does a cluster decide whose job runs when? (fifo vs backfill) | 12 min |
| 5 | Your own code: the biggest lever of all (fix a wasteful bioinformatics pipeline step by step) | 15 min |

Cells marked **(bonus)** can be skipped if you are short on time.

## How to use it

1. Click the **Open in Colab** badge above.
2. Run the cells **top to bottom** (`Shift + Enter`). The first code cell ("Setup") must be run first.
3. Questions marked 🎯 are meant to be answered *before* you run the cell. Solutions are hidden behind 🔍, so try first.

You mostly move sliders and run cells; there is almost no code to write.

## Notes

- **Colab has 2 CPU cores**, so the real parallel speedups in Parts 1 and 5 top out at about 2×. Parts 2 to 4 are simulations that explore what happens with 100 or 1000 cores.
- Part 1 creates a small helper file (`hpc_workers.py`) and Part 5 creates some sequence files (`sequences_*.fasta`) in the Colab session. They disappear when the session ends.
- Part 5 may take a minute or two on Colab (the original code is deliberately slow).
- If something behaves oddly, use **Runtime → Restart session** and run the cells again from the top.

## Running locally (optional)

```bash
pip install numpy matplotlib ipywidgets jupyterlab
jupyter lab hpc_exercise.ipynb
```

Python 3.9+ on Linux or macOS. On Windows, Parts 1 and 5 (multiprocessing) are best run in Colab or WSL.

## Contact

Jakob Steuer · FHNW School of Life Sciences, Institute for Chemistry and Bioanalytics ·
