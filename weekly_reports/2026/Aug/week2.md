# Week 2

## fgvc — Prototype-Based Fine-Grained Visual Classification

A dataset-agnostic pipeline for prototype/retrieval-based fine-grained
visual classification: fine-tune a backbone, build a per-class prototype
memory with Spherical K-Means, and classify new images by cosine-similarity
retrieval against that memory (with open-set "unknown" detection).


## Architecture Overview

```
Query Image
    │
    ▼
┌─────────────────────────────────────────────────────────┐
│  Backbone (any timm model, fine-tuned)                   │
│  → L2-normalised embedding  (e.g. 768-D for ViT-B/14)     │
└──────────────────────────────┬───────────────────────────┘
                                │
                                ▼
┌────────────────────────────────────────────────────────────┐
│  Prototype Memory  (Spherical K-Means)                      │
│  Per label_id (the fine-grained class): K centroids on S^d  │
└──────────────────────────────┬───────────────────────────────┘
                                │  cosine similarity + MAX pool
                                ▼
┌────────────────────────────────────────────────────────────┐
│  RetrievalEngine                                             │
│  Ranked list of (label_id, group, label, score) + open-set   │
└────────────────────────────────────────────────────────────┘
```

### WANDB Plots

- CIFAR : [W&B Report](https://api.wandb.ai/links/maitreya-cse-iit-bombay/t7r09umd)

- CUB : [W&B Report](https://api.wandb.ai/links/maitreya-cse-iit-bombay/kkw8x9wu)

---

### RESULTS - CIFAR

- [Metrics](../../../experiments/fgvc/results/cifar100/baseline/outputs/evaluation)
- [Visualization](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations)

#### Visualizations

- [Failure Cases](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/failure_cases_test.png)
- [Retrieval Grid — Test](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/retrieval_grid_test.png)
- [Retrieval Grid — Validation](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/retrieval_grid_val.png)
- [t-SNE — Test](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/tsne_group_test.png)
- [t-SNE — Validation](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/tsne_group_val.png)
- [UMAP — Test](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/umap_label_id_test.png)
- [UMAP — Validation](../../../experiments/fgvc/results/cifar100/baseline/outputs/visualizations/umap_label_id_val.png)
- [Confusion Matrix — Interactive](https://maitreyashelare.github.io/research-notes/experiments/fgvc/results/cifar100/baseline/outputs/visualizations/confusion_matrix_test.html)

#### Other Results

- [Logs](../../../experiments/fgvc/results/cifar100/baseline/logs)
- [Evaluation Metrics](../../../experiments/fgvc/results/cifar100/baseline/outputs/evaluation/test_metrics.json)
- [Test Predictions](../../../experiments/fgvc/results/cifar100/baseline/outputs/evaluation/test_predictions.csv)
- [Validation Metrics](../../../experiments/fgvc/results/cifar100/baseline/outputs/evaluation/val_metrics.json)
- [Validation Predictions](../../../experiments/fgvc/results/cifar100/baseline/outputs/evaluation/val_predictions.csv)
- [Calibration Thresholds](../../../experiments/fgvc/results/cifar100/baseline/outputs/calibration/per_group_thresholds.json)

---

### RESULTS - CUB

- [Metrics](../../../experiments/fgvc/results/cub200/baseline/outputs/evaluation)
- [Visualization](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations)

#### Visualizations

- [Failure Cases](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/failure_cases_test.png)
- [Retrieval Grid — Test](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/retrieval_grid_test.png)
- [Retrieval Grid — Validation](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/retrieval_grid_val.png)
- [t-SNE — Test](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/tsne_label_id_test.png)
- [t-SNE — Validation](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/tsne_label_id_val.png)
- [UMAP — Test](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/umap_label_id_test.png)
- [UMAP — Validation](../../../experiments/fgvc/results/cub200/baseline/outputs/visualizations/umap_label_id_val.png)
- [Confusion Matrix — Interactive](https://maitreyashelare.github.io/research-notes/experiments/fgvc/results/cub200/baseline/outputs/visualizations/confusion_matrix_test.html)

#### Other Results

- [Logs](../../../experiments/fgvc/results/cub200/baseline/logs)
- [Evaluation Metrics](../../../experiments/fgvc/results/cub200/baseline/outputs/evaluation/test_metrics.json)
- [Test Predictions](../../../experiments/fgvc/results/cub200/baseline/outputs/evaluation/test_predictions.csv)
- [Validation Metrics](../../../experiments/fgvc/results/cub200/baseline/outputs/evaluation/val_metrics.json)
- [Validation Predictions](../../../experiments/fgvc/results/cub200/baseline/outputs/evaluation/val_predictions.csv)
- [Calibration Thresholds](../../../experiments/fgvc/results/cub200/baseline/outputs/calibration/per_group_thresholds.json)