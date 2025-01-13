# Climate Change Conversational Chatbot

### Overview

This project focuses on building a conversational chatbot trained on a dataset about climate change. The chatbot leverages the DialoGPT model to answer questions and engage in discussions about climate change. It incorporates fine-tuning techniques to customize the model for this specific domain.

### Problem Statement

Brain tumors are life-threatening conditions that require timely and accurate diagnosis. However, traditional diagnostic processes can be time-intensive, subjective, and prone to errors due to human limitations. With the rise of deep learning, AI models can analyze medical images with remarkable accuracy and speed.

This project aims to classify brain tumors from MRI scans into four categories: glioma, meningioma, no tumor, and pituitary tumor. Additionally, it uses explainability tools to ensure transparency in model predictions, building trust in AI-driven clinical decision-making.

In medical applications, trust and reliability are critical. By highlighting the model’s decision-making process through SHAP and LIME, this project addresses a vital gap in AI adoption in healthcare.

### Dataset

The dataset was designed to build a chatbot that can provide meaningful discussions about climate change. Each entry contains:

- Source: URL or origin of the FAQ.
- faq: The question or answer related to climate change.
- text_type: A tag indicating whether the entry is a question (q) or an answer (a).

The dataset is structured sequentially, ensuring that each question is followed by its corresponding answer.

### Features

- Fine-Tuned DialoGPT: A pre-trained conversational model fine-tuned on a climate change FAQ dataset.
- Real-Time Interaction: Includes a chatbot interface for real-time interactions.
- BLEU Score Evaluation: Measures the quality of generated responses against reference answers using BLEU scores.
- Model Export: Saves the fine-tuned model and tokenizer for future deployment.

### Solution Approach

Step 1: Data Cleaning and Preparation
- Preprocessing Techniques:
    - Resized MRI images to a uniform dimension for model consistency.
    - Normalized pixel intensity values to improve training stability.
    - Applied data augmentation (e.g., rotation, flipping, cropping) to address class imbalances and enhance model robustness.

- Handling Class Imbalance:
    - Balanced the dataset by applying class weights during model training to ensure fair representation of all tumor categories.

Step 2: Exploratory Data Analysis (EDA)
- Visualized the distribution of tumor types to uncover class imbalances.
- Analyzed pixel intensity histograms to ensure image consistency.
- Generated heatmaps to examine inter-class variability and highlight common patterns.

Step 3: Feature Engineering
- Extracted spatial features using convolutional layers in CNNs.
- Augmented training data with variations to simulate real-world scenarios.
- Enhanced model robustness by focusing on key tumor-specific regions in the MRI images.

Step 4: Model Building
- Architecture Selection: Used a CNN-based architecture optimized for image classification.
- Hyperparameter Tuning: Experimented with learning rates, batch sizes, and dropout rates to optimize model performance.
- Evaluation Metrics: Measured accuracy, precision, recall, and F1-score across all classes.

Step 5: Explainability with SHAP and LIME
- SHAP: Generated heatmaps to identify which parts of an image contributed most to the model’s classification.
- LIME: Highlighted the critical regions influencing individual predictions, providing interpretable boundaries around the tumor regions.

Step 6: Testing and Evaluation
- Performance Analysis: Achieved 69% overall accuracy, with strengths in classifying no tumor and pituitary tumor cases.
- Challenges Identified: Lower recall for meningioma classification highlighted the need for further class balancing and fine-tuning.
- Visual Insights: Created confusion matrices to showcase model performance and identify misclassifications.

### Results

- BLEU Score: 0.0050 (indicative of basic performance; requires further fine-tuning and dataset enrichment).
- The chatbot demonstrates basic conversational capabilities, responding meaningfully to some inputs but may require further improvement for broader use cases.

### Key Findings

- Strengths: High accuracy in detecting “No Tumor” and “Pituitary Tumor” classes.
- Challenges: Underperformance in “Meningioma” classification due to data imbalance.
- Impact: Demonstrated the feasibility of using CNNs for medical image classification with transparent decision-making.

### Future Directions

- Incorporate Real-Time Data: Extend the model to analyze live MRI scans for real-time diagnostics.
- Enhance Data Diversity: Use larger, more diverse datasets to improve generalization across demographics.
- Expand Explainability: Combine SHAP and LIME with Grad-CAM to provide more granular explanations.
- Clinical Integration: Test the model in a clinical setting to evaluate its performance under real-world conditions.

### Source

https://www.kaggle.com/datasets/ishgirwan/climate-change-faqs/data
