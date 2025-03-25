# Predicting machine learning algorithm performance in real life
### 1. Topic:
Medical Imaging/CV

### 2. Background:
Often time in machine learning, real-world data may be different from the training and testing data. If we have ample real-life data, we can of course directly test our algorithm on the test data, and evaluate its real-life performance. In practice, however, we often have little to no labelled real-life data. Recently, a paper proposed to predict out-of-distribution (OOD) performance by leveraging unlabelled data for generic imaging datasets like ImageNet.

### 3. Research Question:
Can we extend that work to predict the OOD performance in medical imaging datasets? For example, from one hospital to another in Camelyon17, or from one xray dataset to another in ChestXray & CheXpert?

### 4. Expected work:
Run experiments to assess OOD prediction performance among the Camelyon17 datasets and the ChestXray & CheXpert datasets.

### 5. Bonus:
Collaboration/Internship possible with GSK


# Investigating calibration performance in LLMs
### 1. Topic:
LLM/NLP

### 2. Background:
Investigating calibration performance is an important step in assessing the reliability and trustworthiness of LLMs. Calibration refers to the evaluation of the model's predictive probabilities against the true outcomes. In the context of LLMs, calibration plots (e.g. ECE) measures how close the LLM token probabilities are to the actual probabilities. If a model is well-calibrated, it means that if we take all instances where the model predicts a probability of, say, 0.8, then 80% of those instances should be correct. To investigate calibration performance in LLMs, we can use calibration plots (also known as reliability diagrams). In these plots, the predicted probabilities are grouped into bins, and for each bin, the mean predicted probability is plotted against the actual fraction of positives. A perfectly calibrated model would result in a plot where all points lie along the diagonal line. The reason that calibration performance is especially interesting for LLMs is twofold: (1) In the GPT-4 technical report released by OpenAI, a significant degradation in ECE is observed going from the pretrained model to the finetuned model, i.e. RLHF seems to nullify the LLM token probabilities (2) Free-form responses produced by the LLM are often not verifiable. This is where good calibration can really help, because if the LLM is correctly confident about its answers, then the confidence score is in some sense, a verifier score.

### 3. Research Question:
Under what circumstances do LLM exhibit good calibration, and how can we improve LLM calibration?

### 4. Expected work:
Run experiments to measure calibration performance in various LLMs, which could vary in architecture, decoding technique, training algorithm, etc.

### 5. Bonus:
Collaboration possible with ongoing LLM work in the English Faculty


# Conditional generation in tabular data models
### 1. Topic:
Tabular Data/Diffusion models

### 2. Background:
Tabular data research likes to focus on prediction problems—predicting the target column values based on the other columns—because that is commonly required in real life in medicine, finance, etc. A less studied, and arguably more interesting problem, is conditional generation in tabular data. Conditional generation refers to the process of generating new data rows or instances based on specific conditions or given values for some features. This is a significant area in AI research, especially in the fields of data augmentation, synthetic data generation, and privacy-preserving data publishing. The primary goal of conditional generation is to create new tabular data that maintains the statistical properties of the original data while satisfying the given conditions. This involves predicting the values of the remaining features given the values for a subset of features. These models are trained on the original data, and then they can generate new data that follows the same distribution. However, conditional generation in tabular data models is challenging because tabular data often contains a mix of numerical and categorical features, and it can have complex dependencies between features. One of the most popular tabular data models is TabDDPM.

### 3. Research Question:
Can we assess various aspects of TabDDPM’s conditional generation performance in tabular data, and what are some ways we can improve it?

### 4. Expected work:
Run experiments to evaluate generation performance of TabDDPM under various metrics such as downstream classifier, discriminator, coverage, etc.
