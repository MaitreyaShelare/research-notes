# Week 3
## FGVC — Prototype-Based Fine-Grained Visual Classification

### Actions Taken
- Trained Model End-to-End with different params, hyperparams, losses
- Two Candidate Models - v9 and v13

### Observations
- Having more number of prototypes, in general, improves accuracy and reduces ambiguity
- Will need to work on ranking top 3, new loss, or new block addition - To find out

## FGVC Results

### WANDB Plots

- CUB v9 and v13 : [W&B Report](https://api.wandb.ai/links/maitreya-cse-iit-bombay/in42np5v)

---

### RESULTS - CUB200 — DINOv3 CE SupCon v9

- [Config Snapshot](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/config_snapshot.yaml)
- [Test Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation/test_metrics.json)

- [All Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation)
- [All Visualizations](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations)

#### Visualizations

- [Failure Cases](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/failure_cases_test.png)
- [Retrieval Grid — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/retrieval_grid_test.png)
- [Retrieval Grid — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/retrieval_grid_val.png)
- [t-SNE — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/tsne_label_id_test.png)
- [t-SNE — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/tsne_label_id_val.png)
- [UMAP — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/umap_label_id_test.png)
- [UMAP — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/umap_label_id_val.png)
- [Confusion Matrix — Interactive](https://maitreyashelare.github.io/research-notes/experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/visualizations/confusion_matrix_test.html)

#### Other Results

- [Logs](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/logs)
- [Evaluation Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation/test_metrics.json)
- [Test Predictions](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation/test_predictions.csv)
- [Validation Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation/val_metrics.json)
- [Validation Predictions](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/evaluation/val_predictions.csv)
- [Calibration Thresholds](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v9/outputs/calibration/per_group_thresholds.json)

---
### RESULTS - CUB200 — DINOv3 CE SupCon v13


- [Config Snapshot](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/config_snapshot.yaml)
- [Test Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation/test_metrics.json)

- [All Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation)
- [All Visualizations](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations)


#### Visualizations

- [Failure Cases](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/failure_cases_test.png)
- [Retrieval Grid — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/retrieval_grid_test.png)
- [Retrieval Grid — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/retrieval_grid_val.png)
- [t-SNE — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/tsne_label_id_test.png)
- [t-SNE — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/tsne_label_id_val.png)
- [UMAP — Test](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/umap_label_id_test.png)
- [UMAP — Validation](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/umap_label_id_val.png)
- [Confusion Matrix — Interactive](https://maitreyashelare.github.io/research-notes/experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/visualizations/confusion_matrix_test.html)

#### Other Results

- [Logs](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/logs)
- [Evaluation Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation/test_metrics.json)
- [Test Predictions](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation/test_predictions.csv)
- [Validation Metrics](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation/val_metrics.json)
- [Validation Predictions](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/evaluation/val_predictions.csv)
- [Calibration Thresholds](../../../experiments/fgvc/results/cub200/cub200_dinov3_ce_supcon_v13/outputs/calibration/per_group_thresholds.json)

-----
## FAVS — Fine-Grained Audio Visual Segmentation

### Actions Taken
- Studied about the problem of AVS - Given a video, determine whether the audio has a visible source in the scene, and if so, identify and segment the visible source.
- Studied three settings - S4 (Single Sound Source
Segmentation), MS3 (Multiple Sound Source
Segmentation), AVSS (Audio-Visual Semantic
Segmentation)

### Actions to do
- Identified two possible directions - Robustness & Real-time inference, decided on Robustness after discussion
- Found Relevant paper on Robustness - AAAI 2026 - [text](https://ojs.aaai.org/index.php/AAAI/article/view/37542)