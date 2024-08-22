# **Replication material and Appendix for the paper "Synthetic Product Review Generation for Market Analysis: A GPT-2 and LLaMA 3 Approach"**
**Description:** This repository contains the replication materials and the Appendix for our final project for the course "Deep Learning for the Social Sciences" (SuSe 2024) at the University of Konstanz.

**Authors:** George-Lembach, Carl, Klotz, Tom, Schleißheimer, Julia, and Velev, Valentin

## Appendix
The Appendix for our paper is available in the file [appendix.pdf]().

## Fine-Tuned GPT-2 Medium
Our fine-tuned GPT-2 Medium model is available on [Hugging Face](https://huggingface.co/TomData/GPT2-review).

Nore that since we used PyTorch to fine-tune GPT-2 Medium, the Inference API on Hugging Face does not work.

## Data
In the folder [Data](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/tree/main/Data), we have made available our four main datasets. The remaining datasets are available on [Synology Cloud](https://T34278926.quickconnect.to/d/s/ziemTGVVHGhyI6UHtWm7P9qA4fkL730m/d_yA3FB3AKlZC2PuJi0EphdTXlMTogjB-K7Ug0fCgmws ). Below you will find a brief overview of all files in the folder:

* [preprocessed_reviews.csv](): ...
* [topic_modeling_results.csv](): ...
* [gpt-2_synthetic_reviews.csv](): ...
* [gpt-2_synthetic_reviews_human_eval_sample.csv](): ...
* [gpt-2_tested_prompts.csv](): ...
* [llama-3_synthetic_reviews.csv](): ...
* [llama-3_synthetic_reviews_human_eval_sample.csv](): ...
* [llama-3_tested_prompts.csv](): ...
* [human_evaluation.xlsx](): ...
* [market_analysis.xlsx](): ...

## Notebooks
In the folder [Notebooks](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/tree/main/Notebooks), we have made available the Jupyter Notebooks we used for all our computation, analysis, and visualization. Below you will find a brief overview of all files in the folder:

* [ETL.ipynb](): Notebook for data preprocessing / extract-transform-load (ETL) pipeline including:
  * Data cleaning
  * ...
  * ...
* [EDA.ipynb](): Notbook for exploratory data analysis (EDA) including:
  * Average length of reviews and standard deviation of review length
  * Histogram of review length distribution
  * Rating distribution (overall and by sentiment)
  * Word clouds (overall, by sentiment, and by rating)
  * Topic modeling using BERTopic
* [topic_modeling.ipynb](): Notebook for topic modelling using BERTopic.
* [gpt-2_fine-tune.ipynb](): Notebook for fine-tuning GPT-2. Note that the fine-tuning with 100,000 reviews takes roughly 2-3 days using two NVIDIA A40 GPUs (48 GB).
* [gpt-2_review_generation.ipynb](): Notebook for generating synthetic product reviews using GPT-2 Medium and calculating perplexity.
* [llama-3_review_generation.ipynb](): Notebook for generating synthetic product reviews using LLaMA 3 8B and calculating perplexity. Note that the initialization of LLaMA 3 8B in Kaggle with an NVIDIA P100 GPU (16GB) takes roughly 50 minutes and the generation of 10,000 synthetic reviews takes roughly 20 hours.
* [stat_evaluation.ipynb](): Notebook for the statistical evaluation of the synthetic product reviews, including:
  * Statistical tendencies (Zipf's law)
  * Linguistic features (average length, type-token ratio, verb and noun usage, and readability)
  * MAUVE
  * Inter-rater reliability and PERMANOVA (for human evaluation)

## Plots
In the folder [Plots](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/tree/main/Plots), we have uploaded all our plots. Below you will find a brief overview of all files in the folder:

Paper:
* [rating_distribution.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/rating_distribution.pdf): Figure 1 (left side) &ndash; Rating distribution
* [rating_distribution_sentiment.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/rating_distribution_sentiment.pdf): Figure 1 (right side) &ndash; Rating distribution by sentiment
* [wordcloud.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud.pdf): Figure 2 &ndash; Word cloud of all real reviews

Appendix:
* [hist_rev_len.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/hist_rev_len.pdf): Figure A1 &ndash; Review length distribution
* [wordcloud_pos.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_pos.pdf): Figure A2 (top) &ndash; Word cloud of reviews classified as positive 
* [worcloud_neg.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_neg.pdf): Figure A2 (bottom) &ndash; Word cloud of reviews classified as negative
* [wordcloud_rating1.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_rating1.pdf): Figure A3 (top left) &ndash; Word cloud of reviews with a rating 1/5
* [wordcloud_rating2.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_rating2.pdf): Figure A3 (top right) &ndash; Word cloud of reviews with a rating 2/5
* [wordcloud_rating3.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_rating3.pdf): Figure A3 (middle left) &ndash; Word cloud of reviews with a rating 3/5
* [wordcloud_rating4.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_rating4.pdf): Figure A3 (middle right) &ndash; Word cloud of reviews with a rating 4/5
* [wordcloud_rating5.pdf](https://github.com/valentin-velev29/DLSS-24-Project-Replication-Material/blob/main/Plots/wordcloud_rating5.pdf): Figure A3 (bottom) &ndash; Word cloud of reviews with a rating 5/5
