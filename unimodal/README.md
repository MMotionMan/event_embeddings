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
| **CoLES embeds + WinAgg (5 trx)**     | 0.7327 ± 0.0025       | 0.8094 ± 0.0045 |
| **CoLES embeds + WinAgg (7 trx)**     | 0.7393 ± 0.0062       | 0.8076 ± 0.0039 |
| **CPC Modeling (emb_dim=32)**         | 0.747 ± 0.0041        | 0.8099 ± 0.0035 |
| **CPC Modeling (emb_dim=32) + WinAgg**| 0.748 ± 0.0071        | 0.8111 ± 0.0058 |
| **CPC Modeling (emb_dim=8)**          | 0.747 ± 0.0052        | 0.8165 ± 0.0032 |
| **CPC Modeling (emb_dim=8) + WinAgg** | 0.734 ± 0.0257        | 0.8045 ± 0.0087 |
| **TD-GPT**                            | 0.73 ± 0.0049         | 0.7949 ± 0.0065 |
| **TD-GPT + WinAgg (multilabel loss)** | 0.732 ± 0.0201        | 0.7957 ± 0.0115 |

----

**Aggregation by Days:**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**                            | 0.67 ± 0.0046         | 0.7536 ± 0.003  |
| **GRU (+ MLP)**                                    | 0.746 ± 0.0076        | 0.8148 ± 0.0037 |
| **CoLES**                                          | 0.726 ± 0.0071        | 0.8076 ± 0.0025 |
| **CoLES embeds + AggByDays (1 day)**               | 0.742 ± 0.0156        | 0.8116 ± 0.003  |
| **CPC Modeling (emb_dim=32)**                      | 0.747 ± 0.0041        | 0.8099 ± 0.0035 |
| **CPC Modeling (emb_dim=32) + AggByDays (2 days)** | 0.744 ± 0.0065        | 0.8204 ± 0.0016 |
| **CPC Modeling (emb_dim=8)**                       | 0.747 ± 0.0052        | 0.8165 ± 0.0032 |
| **CPC Modeling (emb_dim=8) + AggByDays (2 days)**  | 0.7367 ± 0.0025       | 0.813 ± 0.0094  |
| **TD-GPT**                                         | 0.73 ± 0.0049         | 0.7949 ± 0.0065 |
| **TD-GPT + AggByDays**                             |   -                   | -               |


----

**Convolutional Aggregation (overlapping windows):**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**                | 0.67 ± 0.0046         | 0.7536 ± 0.003  |
| **GRU (+ MLP)**                        | 0.746 ± 0.0076        | 0.8148 ± 0.0037 |
| **CoLES**                              | 0.726 ± 0.0071        | 0.8076 ± 0.0025 |
| **COLES embeds + ConvAgg (7 trx)**     | 0.7393 ± 0.0133       | 0.8122 ± 0.0128 |
| **CPC Modeling (emb_dim=32)**          | 0.747 ± 0.0041        | 0.8099 ± 0.0035 |
| **CPC Modeling (emb_dim=32) + ConvAgg**| 0.7507 ± 0.0057       | 0.8179 ± 0.0061 |
| **CPC Modeling (emb_dim=8)**           | 0.747 ± 0.0052        | 0.8165 ± 0.0032 |
| **CPC Modeling (emb_dim=8) + ConvAgg** | 0.7293 ± 0.0074       | 0.8068 ± 0.0075 |
| **TD-GPT**                             | 0.73 ± 0.0049         | 0.7949 ± 0.0065 |
| **TD-GPT + ConvAgg**                   | 0.722 ± 0.0278        | 0.7896 ± 0.0181 |

----

# Age Prediction Dataset:

**Baselines:**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences** | 0.4921 ± 0.005    | 0.76 ± 0.0012     |
| **GRU (+ MLP)**         | 0.6066 ± 0.0019   | 0.8479 ±  0.0013  |
| **CoLES**               | 0.6042 ± 0.0083   | 0.8482 ± 0.0007   |
| **CPC Modeling**        | 0.5762 ± 0.0058   | 0.8305 ± 0.003    |
| **GPT2**                | 0.6146 ± 0.0075   | 0.852 ± 0.0029    |

----

**Window Aggregation (non-overlapping windows):**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**                   | 0.4921 ± 0.005        | 0.76 ± 0.0012   |
| **GRU (+ MLP)**                           | 0.6066 ± 0.0019       | 0.8479 ± 0.0013 |
| **CoLES**                                 | 0.6042 ± 0.0083       | 0.8482 ± 0.0007 |
| **CoLES embeds + WinAgg (3 trx)**         | 0.5848 ± 0.0023       | 0.8334 ± 0.0011 |
| **CPC Modeling**                          | 0.5762 ± 0.0058       | 0.8305 ± 0.003  |
| **CPC Modeling + WinAgg (3 trx)**         | 0.5842 ± 0.0059       | 0.8335 ± 0.0014 |
| **GPT2**                                  | 0.6146 ± 0.0075       | 0.852 ± 0.0029  |
| **GPT2 + WinAgg (4 trx, next N trx loss)**| 0.5991 ± 0.0023       | 0.8425 ± 0.0005 |

----

**Aggregation by Days:**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**                              | 0.4921 ± 0.005        | 0.76 ± 0.0012   |
| **GRU (+ MLP)**                                      | 0.6066 ± 0.0019       | 0.8479 ± 0.0013 |
| **CoLES**                                            | 0.6042 ± 0.0083       | 0.8482 ± 0.0007 |
| **CoLES embeds + AggByDays (1 day, w/ Null Tokens)** | 0.5966 ± 0.004        | 0.8425 ± 0.0012 |
| **CPC Modeling**                                     | 0.5762 ± 0.0058       | 0.8305 ± 0.003  |
| **CPC Modeling + AggByDays (2 days)**                | 0.5682 ± 0.0052       | 0.8236 ± 0.0027 |
| **GPT2**                                             | 0.6146 ± 0.0075       | 0.852 ± 0.0029  |
| **GPT2 + AggByDays**                                 | -                     | -               |

----

**Convolutional Aggregation (overlapping windows):**

| Method|Accuracy|ROC-AUC|
| --- |:---:|:---:|
| **Flattened Sequences**                   | 0.4921 ± 0.005        | 0.76 ± 0.0012   |
| **GRU (+ MLP)**                           | 0.6066 ± 0.0019       | 0.8479 ± 0.0013 |
| **CoLES**                                 | 0.6042 ± 0.0083       | 0.8482 ± 0.0007 |
| **COLES embeds + ConvAgg (3 trx)**        | 0.6027 ± 0.0023       | 0.8461 ± 0.0013 |
| **CPC Modeling**                          | 0.5762 ± 0.0058       | 0.8305 ± 0.003  |
| **CPC Modeling + ConvAgg (5 trx)**        | 0.585 ± 0.0043        | 0.8317 ± 0.0018 |
| **GPT2**                                  | 0.6146 ± 0.0075       | 0.852 ± 0.0029  |
| **GPT2 + ConvAgg ()**                     | 0.6128 ± 0.0019       | 0.8523 ± 0.0015 |