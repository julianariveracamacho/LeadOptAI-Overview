# LeadOptAI

**Chemistry-aware molecular machine learning for property prediction and SMILES infilling**

LeadOptAI is a research project developed by **Juliana Rivera Camacho** as part of a master’s thesis in Molecular Life Sciences at Universität Hamburg.

This public repository introduces the project and documents the organization of its private research implementation. It contains documentation only. Source code, trained weights, datasets and detailed experimental results are not distributed here while the work is being prepared for publication.

## Research motivation

Molecular optimization requires balancing physicochemical properties while considering chemical structure. LeadOptAI investigates whether chemically informed reconstruction tasks can help a Transformer learn relationships between molecular representations and continuous property information.

## Project overview

The framework combines:

- A bidirectional Transformer encoder for SMILES representations.
- Separate embeddings for discrete tokens and continuous molecular descriptors.
- Joint masked-token reconstruction and molecular-property prediction.
- Single-token, contiguous-block, functional-group and BRICS fragment masking.
- Experimental comparison of masking strategies and optional atom-level features.

The molecular descriptors considered are molecular weight, LogP, rotatable bonds, topological polar surface area, hydrogen-bond donors and hydrogen-bond acceptors.

## Why chemistry-aware masking?

Functional-group and BRICS masking select recognizable chemical units for reconstruction. Together with token and block masking, they provide learning tasks at several structural scales. The research examines how these objectives support molecular representation learning and the investigation of localized molecular editing.

## My contribution

I developed the model and molecular-data workflow, implemented chemistry-informed masking, conducted training and evaluation experiments, compared molecular language-model baselines, and analyzed and communicated the results.

**Technology:** Python · PyTorch · RDKit · SMILES · SMARTS · BRICS

## Implementation structure

[CODE_STRUCTURE.md](CODE_STRUCTURE.md) describes the main files in the private research implementation and their responsibilities. It is a navigation map, not executable source code. The listed Python files are deliberately absent from this public repository.

## Scientific scope

The evaluated infilling setup used properties associated with the source molecule. It therefore examines reconstruction and preservation of the source property profile. Control toward intentionally changed property targets remains a separate validation task. Physicochemical descriptors do not establish biological activity or a full ADMET profile.

## Research and publication status

This work is being prepared for scientific publication. Please acknowledge the researchers’ contributions and contact the author to discuss collaboration or access to unpublished material. Publication details and any future release information will be added when available.

This overview does not grant access to the private implementation or introduce a license for it. Third-party rights remain applicable.

## Author

**Juliana Rivera Camacho** · Universität Hamburg · Hamburg, Germany

[GitHub profile](https://github.com/julianariveracamacho)
