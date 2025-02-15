# FLEX
**Knowledge-Guided Adaptation of Pathology Foundation Models Improves Cross-domain Generalization and Demographic Fairness**

**Abstract:** The advent of foundation models has ushered in a transformative era in computational pathology, enabling the extraction of rich, transferable image features for a broad range of downstream pathology tasks. However, site-specific signatures and demographic biases persist in these features, leading to short-cut learning and unfair predictions, ultimately compromising model generalizability and fairness across diverse clinical sites and demographic groups. In this paper, we propose FLEX, a novel framework that enhances cross-domain generalization and demographic fairness of pathology foundation models, thus facilitating accurate diagnosis across diverse pathology tasks. FLEX employs a task specific information bottleneck, informed by visual and textual domain knowledge, to promote generalizability across clinical settings, fairness across demographic groups, and adaptability to specific pathology tasks. We evaluate FLEX on 16 clinically relevant tasks across three categories, including morphology classification, molecular biomarker status prediction, and gene mutation prediction, using four TCGA cohorts. Experimental results show that FLEX significantly improves diagnostic performance on data from unseen sites, reduces the performance gap between seen and unseen sites, and enhances fairness across demographic groups compared to baseline methods. Moreover, FLEX demonstrates high versatility, compatibility across various vision-language models, scalability to varying training data sizes, and seamless integration with multiple instance learning frameworks. These findings underscore the potential of FLEX to advance both the cross-domain generalization and demographic fairness of pathology foundation models, fostering more robust and equitable computational pathology systems.

![main_figure](fig/main_v14.png)

## Generate SP-MCCV split

```bash
python create_splits_seq_sitepre_kandfold.py
```

## Run FLEX with CONCH

```bash
bash ./scripts/train_flex.sh
```