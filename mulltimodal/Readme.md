# Overview

This repository contains files for A.V. Kirichenko's thesis. 

Description of the main files:

	- ![[datafusion_exps+baseline.ipynb]] - This file contains experiments for a multimodal task formulation with the dataset Data Fusion Contest 2022.
- ![[mbd-my-code-multimodal.ipynb]] - This file describes all experiments with multimodal data from the MBD dataset.
	- ![[datafusion2024.ipynb]] - Unimodal experiments for the data set Data Fusion Contest 2024.
- ![[mbd-unimodal.ipynb]] - Unimodal experiments with MBD dataset.
	- ![[mbd-transformers.ipynb]] - Application of transformer architectures for unimodal data from MBD.
	- ![[datafusion2022unimodal.ipynb]] - Experiments with unimodal data from the dataset Data Fusion Contest 2022.

All other files contain experiments that were not included in the main work, such as time aggregations, testing of various aggregation methods after SWIN, and various groupings of source data. They also contain accompanying material for further research.

# Results 

# DF2022 unimodal

**Baseline**

ROC-AUC target = 0.57

**RnnEncoder with regional-attention**

reg = 5

ROC-AUC target = 0.59

**RnnEncoder with regional-attention**

reg = 10

ROC-AUC target = 0.53

**RnnEncoder with cross-attention**

sm = 5

big = 16

ROC-AUC target = 0.54

**RnnEncoder with cross-attention**

sm = 4

big = 15

ROC-AUC target = 0.54

**RnnEncoder with cross-attention**

sm = 3

big = 12

ROC-AUC target = 0.54

# DF 2024 unimodal

**Baseline (CoLES)**

ROC-AUC target = 0.6885229034842104

accuracy = 0.91

**CoLES + regional-attention**

ROC-AUC target = 0.705245790800391

accuracy = 0.91

**CoLES + cross-attention**

small patches = 4

large patches = 15

ROC-AUC target = 0.6635

accuracy = 0.90

**CoLES + cross-attention**

small patches = 5

large patches = 16

ROC-AUC target = 0.6513

accuracy = 0.90

**CoLES + cross-attention**

small patches = 3

large patches = 12

ROC-AUC target = 0.6671

accuracy = 0.91

**GPT Baseline**

ROC-AUC target = 0.7306271092054157

accuracy = 0.9293908996750897

**GPT With SWIN enc**

ROC-AUC target = 0.7012497152222003

accuracy = 0.909765625

# MBD unimodal transformers

**GPT Baseline (RPE)**

ROC-AUC target0 = 0.721350441667294

ROC-AUC target1 = 0.8153566994158479

ROC-AUC target2 = 0.7543318213719505

ROC-AUC target3 = 0.7678734355960962

**GPT + SWIN encoder (mean agg)**

ROC-AUC target0 = 0.6516282035967174

ROC-AUC target1 = 0.6540494938132733

ROC-AUC target2 = 0.5948775519632066

ROC-AUC target3 = 0.745110173028166

**CoLES + SWIN + mean**

ROC-AUC target0 = 0.7036866820699578

ROC-AUC target1 = 0.6407223242752476

ROC-AUC target2 = 0.6655641307690068

ROC-AUC target3 = 0.7021158878362178


**CoLES + SWIN + RNN**


ROC-AUC target0 = 0.6988762517846345

ROC-AUC target1 = 0.8023436653648343

ROC-AUC target2 = 0.6582610542989475

ROC-AUC target3 = 0.7862126496756947

# MBD multimodal regional attention

**CoLES + regional attention in trx (segment_length=10) + LightGBM (Without LN):**

ROC-AUC target0 = 0.6674023787783245

ROC-AUC target1 = 0.8062314626627639

ROC-AUC target2 = 0.5838852723065378

ROC-AUC target3 = 0.6902740886029226

**CoLES + regional attention in trx + LightGBM (With LN):**

ROC-AUC target0 = 0.6835130424746901

ROC-AUC target1 = 0.7069505322479649

ROC-AUC target2 = 0.5838252484700381

ROC-AUC target3 = 0.6956062235064757


**CoLES + regional attention in trx + LightGBM (Witр BN):**

ROC-AUC target0 = 0.5941521400656775

ROC-AUC target1 = 0.72975601217508

ROC-AUC target2 = 0.5737223564128565

ROC-AUC target3 = 0.618690245938203

**CoLES + regional attention in trx (segment_length=5) (With LN)**

ROC-AUC target0 = 0.702929348375156

ROC-AUC target1 = 0.5948162619622575

ROC-AUC target2 = 0.576047203889645

ROC-AUC target3 = 0.7450892857142857

# MBD Multimodal all

**CoLES matching modalities + catboost:**

ROC-AUC target0 = 0.6699599097659235

ROC-AUC target1 = 0.7192989323312756

ROC-AUC target2 = 0.5470934676077868

ROC-AUC target3 = 0.7065072821784862


**CoLES matching modalities + LGBM**

ROC-AUC target0 = 0.6661180107103395

ROC-AUC target1 = 0.7134405475530108

ROC-AUC target2 = 0.6401834284943577

ROC-AUC target3 = 0.7121417364725656

**MHA ниже по сути считались не как cross-attention, a как два последовательных attention слоя**

**CoLES matching + MHA + LGBM**

ROC-AUC target0 = 0.5973939920184231

ROC-AUC target1 = 0.6659612192446407

ROC-AUC target2 = 0.5862259818008844

ROC-AUC target3 = 0.5714316887516014


**CoLES mathcing + MHA + HEAD (HEAD FROM ptls.nn) + LGBM (35 iter)**

ROC-AUC target0 = 0.5941521400656775

ROC-AUC target1 = 0.72975601217508

ROC-AUC target2 = 0.5737223564128565

ROC-AUC target3 = 0.618690245938203

***

**CoLES matching + MHA + HEAD (HEAD FROM ptls.nn) + LGBM(50 iter)**


ROC-AUC target0 = 0.5649531001156886

ROC-AUC target1 = 0.6053764293498594

ROC-AUC target2 = 0.5342114538096387

ROC-AUC target3 = 0.6009831802884249


**CoLES matching + cross-attention + LGBM**

ROC-AUC target0 = 0.5738291160821928

ROC-AUC target1 = 0.49745850854433205

ROC-AUC target2 = 0.5466672408356286

ROC-AUC target3 = 0.5899366396133057


**CoLES matching + cross-attention + MLP + LGBM**

**(4 heads)**

ROC-AUC target0 = 0.5738218515775905

ROC-AUC target1 = 0.7087090798242084

ROC-AUC target2 = 0.537503557831869

ROC-AUC target3 = 0.5516268758849778

**(8 heads)**

ROC-AUC target0 = 0.6203291443177379

ROC-AUC target1 = 0.5641793238295452

ROC-AUC target2 = 0.571716778145767

ROC-AUC target3 = 0.6215866737471261

# DF2022 multimodal

**Baseline**

MRR = 0.016

**CoLES**

MRR = 0.011

**CoLES + cross-attention**

MRR = 0.019

**CoLES + ragional-attention**

MRR = 0.015
