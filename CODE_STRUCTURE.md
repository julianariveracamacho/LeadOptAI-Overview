# Private implementation: code structure

This document describes the research implementation at a high level. The Python files below are **not included** in this public overview.

| Private path | Responsibility |
| --- | --- |
| `For_loop_masking_B.py` | Training experiments comparing masking configurations |
| `For_loop_atom_features_A.py` | Experiments involving atom-feature representations |
| `src/smiles_encoder.py` | Main molecular Transformer encoder |
| `src/smiles_encoder_atom_features.py` | Encoder variant using atom-level features |
| `src/masking_functions.py` | Molecular masking operations |
| `src/functional_groups.py` | Functional-group recognition using SMARTS |
| `src/BRICS.py` | BRICS fragmentation and related processing |
| `src/atom_features.py` | Atom-feature representation |
| `src/imports.py` | Shared imports |
| `src/utilities.py` | Supporting workflow utilities |
| `src/other_functions.py` | Additional helper functions |

## Conceptual workflow

1. Prepare molecular structures and physicochemical descriptors.
2. Encode SMILES tokens and continuous numerical values.
3. Select and apply a masking strategy.
4. Train joint molecular reconstruction and property-prediction objectives.
5. Evaluate on held-out data and compare experimental configurations.

Exact algorithms, parameter settings, training data, checkpoints and detailed results remain outside this public repository.
