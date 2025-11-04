# Algebraic-Construction-Galois-C7

# Cyclic Septic (C7) Polynomials via Gaussian Periods in SageMath

This repo generates defining polynomials for the unique degree-7 subfield of
\(\mathbb{Q}(\zeta_p)\) for primes \(p \equiv 1 \pmod 7\), using Gaussian periods.
It avoids expensive subfields() calls and works well for larger primes.

## Features
- Pure SageMath implementation (`CyclotomicField(p)` + Gaussian periods)
- Streams primes and collects minimal polynomials over \(\mathbb{Q}\)
- Exports results to CSV: prime `p`, polynomial string, and coefficient tuple

## Quick start

### Prereqs
- **SageMath ≥ 10.x** (recommended)
- Python standard library `csv` (bundled)

### Run (simple)
```bash
sage -python src/c7_periods.py --prime-bound 50000 --out data/C7_polynomials.csv
