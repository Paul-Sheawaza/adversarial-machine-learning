# AICS-202 Adversarial Machine Learning - Student Run Record

## Test machine
- OS: Ubuntu 24.04.3 LTS (virtual machine)
- CPU: Intel Core i5-2430M @ 2.40 GHz, 4 CPUs visible to the VM
- Memory: 7.7 GiB
- CPU only; no GPU or cloud services used

## Software
- Python 3.12.3
- numpy 2.5.4, scikit-learn 1.9.1, matplotlib 3.11.2, notebook 7.6.5
- Full list: pip_freeze.txt

## Dataset and split
- scikit-learn load_digits (offline, 1,797 images, 8x8), pixel values divided by 16
- Split: test_size 0.25, random_state 42, stratified (1,347 train / 450 test)
- Model: LogisticRegression(max_iter=600, random_state=42)

## Random seeds
- Global SEED 42 (split and model)
- Lab 03 label corruption: numpy default_rng(2026)
- Lab 03 ten-seed noise check (added by me): seeds 1000-1009
- Lab 04 PGD random start: seed 42

## How to reproduce
cd Labs
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m notebook
Open each notebook in order (Lab 01 to Lab 04) and use Kernel > Restart Kernel and Run All Cells.

## Additions to the supplied notebooks
Each notebook has extra cells at the end, added by me with AI assistance, to save results
and charts to the results folder and to add: Lab 02 extra epsilon 0.05; Lab 03 hash
checks and a ten-seed check; Lab 04 student variant (augmentation epsilon 0.03) and a
transfer check. [Supplied code was not modified. Confirm this is true.]

## Results folder
11 files: lab01 (2), lab02 (4), lab03 (3), lab04 (2).

## Safety
Only the bundled digits dataset and locally trained models were used. No external
systems were tested.
