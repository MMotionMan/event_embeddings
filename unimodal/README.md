# Results


# Rosbank Churn Dataset:

**Baselines:**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**       | 0.67 ± 0.0046         | 0.7536 ± 0.003  |
| **GRU (+ MLP)**               | 0.746 ± 0.0076        | 0.8148 ± 0.0037 |
| **CoLES**                     | 0.726 ± 0.0071        | 0.8076 ± 0.0025 |
| **CPC Modeling (emb_dim=8)**  | 0.747 ± 0.0052        | 0.8165 ± 0.0032 |
| **CPC Modeling (emb_dim=32)** | 0.747 ± 0.0041        | 0.8099 ± 0.0035 |
| **TD-GPT**                    | 0.73 ± 0.0049         | 0.7949 ± 0.0065 |

----

**Window Aggregation (non-overlapping windows):**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**               | 0.67 ± 0.0046         | 0.7536 ± 0.003  |
| **GRU (+ MLP)**                       | 0.746 ± 0.0076        | 0.8148 ± 0.0037 |
| **CoLES**                             | 0.726 ± 0.0071        | 0.8076 ± 0.0025 |
| **COLES embeds + WinAgg (5 trx)**     | 0.7327 ± 0.0025       | 0.8094 ± 0.0045 |
| **COLES embeds + WinAgg (7 trx)**     | 0.7393 ± 0.0062       | 0.8076 ± 0.0039 |
| **CPC Modeling (emb_dim=32)**         | 0.747 ± 0.0041        | 0.8099 ± 0.0035 |
| **CPC Modeling (emb_dim=32) + WinAgg**| 0.748 ± 0.0071        | 0.8111 ± 0.0058 |
| **CPC Modeling (emb_dim=8)**          | 0.747 ± 0.0052        | 0.8165 ± 0.0032 |
| **CPC Modeling (emb_dim=8) + WinAgg** | 0.734 ± 0.0257        | 0.8045 ± 0.0087 |
| **TD-GPT**                            | 0.73 ± 0.0049         | 0.7949 ± 0.0065 |
| **TD-GPT + WinAgg (multilabel loss)** | 0.732 ± 0.0201        | 0.7957 ± 0.0115 |

----