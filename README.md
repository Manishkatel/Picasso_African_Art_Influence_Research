# Detecting Artistic Influence Using Computer Vision

A computational analysis of African mask aesthetics in Pablo Picasso's Black Period paintings using ResNet50 and CLIP.

## Overview

This project applies computer vision techniques to quantify the visual similarity between African face masks and Picasso's Black Period paintings (1907–1909). Using pretrained CNN models and cosine similarity, we provide computational evidence for the long-standing art-historical claim that African sculptural aesthetics influenced Picasso's modernist style.

## Paintings Used
- *Les Demoiselles d'Avignon* (1907)
- *Self-Portrait*, oil on canvas (1907)
- *Head of a Sleeping Woman* (1907)

## Masks Used
- [Cleveland Museum of Art African Face Mask](https://www.clevelandart.org/art/1953.456)
- [Smithsonian African Face Mask](https://www.si.edu/object/face-mask%3Anmafa_85-15-20)

## Methodology
1. **Feature Extraction** — ResNet50 and CLIP used as feature extractors via transfer learning (final classification layer removed)
2. **Similarity Measurement** — Cosine similarity computed between mask and painting embeddings

## Key Results

| Model   | Average Similarity Score |
|---------|--------------------------|
| ResNet  | 0.23 – 0.61              |
| CLIP    | 0.43 – 0.54              |

- ResNet: *Self-Portrait* showed highest similarity (0.61)
- CLIP: *Head of a Sleeping Woman* showed highest similarity (0.54)

## Requirements
```bash
pip install torch torchvision transformers scikit-learn pillow
```

## Usage
```bash
# Extract features and compute similarity
python similarity.py --paintings painting1.jpg painting2.jpg painting3.jpg \
                     --masks mask1.jpg mask2.jpg \
                     --model resnet  # or clip
```

## Authors
**Manish Katel** and **Samantha Sherry**  
The University of Southern Mississippi  
manish.katel@usm.edu · samantha.sherry@usm.edu

## Citation
If you use this work, please cite:
```
Katel, M. and Sherry, S. "Detecting Artistic Influence Using Computer Vision:
A Computational Analysis of African Mask Aesthetics in Pablo Picasso's Paintings."
University of Southern Mississippi, 2026.
```
