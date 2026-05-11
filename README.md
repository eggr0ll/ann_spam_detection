## ANN Spam Detection
### Project Overview
Social engineering attacks via written correspondence, especially email, impose a sense of urgency and persuade users of all ages to perform harmful actions (like providing sensitive login information). This project aims to produce a quantitative estimation of whether a written message is spam or not by providing a risk score with adversarial robustness, explainability, and calibration. 

### Dataset
| Source                | Size    | Class Distribution                 |
| --------              | ------- | -------                            |
| nazario_5_dataset.csv | 3065    | 1500 (49% ham) / 1565 (51% spam)   |
| email_text.csv        | 53668   | 23745 (44% ham) / 29923 (56% spam) |

### Baselines
1. Logistic Regression with TF-IDF
2. Feedforward NN w/ One-hot Encoding
3. Feedforward NN w/ Pre-trained Word Embeddings
4. Feedforward NN w/ Pre-trained Word Embeddings and Attention

### BiLSTM Model Architecture
1. Embedding layer - learn word representations
2. Bidirectional LSTM layer - capture contextual meaning in both directions (better accuracy); might compare with forward-only if time allows
3. Attention layer - computes weighted sum of all hidden states so that the most spam-relevant tokens dominate; also used later for explainability
4. Dense layers - classification
5. Output layer - producing probabilities (risk scores)

### Overall Analysis
1. Risk score
2. Explainability

    1. Attention visualization
    2. LIME
    3. Token occlusion
3. Adversarial robustness
4. Calibration

### Plots
The figures and their corresponding code blocks can be seen in `ANNFinalProject.ipynb`. The code that generates a certain plot can be seen in the cell immediately proceeding each plot.