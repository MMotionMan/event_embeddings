# Results

**Rosbank Churn Dataset:**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**               | 0.67 ± 0.0046         | 0.7536 ± 0.003  |
| **GRU (+ MLP)**                       | 0.746 ± 0.0076        | 0.8148 ± 0.0037 |
| **CoLES**                             | 0.733 ± 0.019         | 0.8057 ± 0.0088 |
| **CPC Modeling**                      | 0.748 ± 0.003         | 0.81 ± 0.0048   |
| **GPT2**                              | 0.73 ± 0.01           | 0.7957 ± 0.0091 |
| **CoLES w/ WinAgg** (best setup)      | 0.727 ± 0.009         | 0.7992 ± 0.0078 |
| **CPC w/ WinAgg** (best setup)        | 0.748 ± 0.006         | 0.8102 ± 0.0102 |
| **GPT w/ WinAgg** (1 next trx pred)   | 0.7188 ± 0.016        | 0.7899 ± 0.0142 |
| **GPT w/ WinAgg** (multilabel pred)   | 0.727 ± 0.012         | 0.7946 ± 0.0156 |

----


