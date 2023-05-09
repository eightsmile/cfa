## Quantitative (Fake Quant) Methods

### Linear

#### BP test

The **Breusch-Pagan** test is a statistical test used to detect the presence of heteroskedasticity in a linear regression model.

$$BP-TestStatistic =  n\times R^2_{residual}$$

#### F-statistics

$$F = \frac{(SSE_{restricted}-SSE_{un-restricted})/(DF_R - DF_U)}{SSE_{unrestricted}/DF_U}$$

$DF_R = n-1$, where $1$ is the constant term, $DF_U = n-k-1$. $SSE_r$ is when restricting all coefficients of regressors to be zero, that would be our Total Sum Squared, and $SSE_u$ is without restriction, and that would be our Residual Sum Squared. 

$$F = \frac{(SST-SSR)/k}{SSR/(n-k-1)}$$

$$F = MSEstimate/MSResidual= \frac{SSE/DF_E}{SSR/DF_R} $$

$$F = \frac{R^2 / k}{(1-R^2 ) / (n-k-1)}$$

#### Leverage Measure

The rule of thumb for the leverage measure is that if it exceeds $3\frac{k+1}{n}$, where $k$ is the number of independent variables.

#### AR Model

$$y_t = \theta_0 + \theta_1 y_{t-1}+\epsilon_t$$

Standard Error for autocorrelation is $\frac{1}{T-k}$,

- $T$ - the number of periods
- $k$ - e.g. for $AR(1)$, $k=1$

Mean Reversion of $AR(1)$ is setting $y_t = y_{t-1}=y_c$, then $y_c = \frac{\theta_0}{1-\theta_1}$

The Series is stationary after taking a first different, then that series is $I(1)$, and thus has an **unit root**.

### Machine Learning

#### Supervised & Un-Supervised

If there is **no known outcome or target variable**, then there should be an **unsupervised ML model**. For unsupervised learning models, **no splitting of the master dataset is needed** (in another words, **no need to split train-set and validation-set of data**), because of the **absence of labeled** training data. Supervised ML datasets (with labeled training data) contain ground truth, the known outcome (target variable) of each observation in the dataset.

#### Type

Ordinal Variable - with ranking, 1st, 2nd, 3rd, etc

Categorical Variable - 0 & 1, etc without ranking

#### Scaling

- **Normalisation** 归一化, rescale to [0,1]. Normalisation is applied when the distribution of data is not known.

$$x_{normalised} = \frac{x_i - x_{min}}{x_{max} - x_min}$$

- **Standardisation** 正态 <- 需要正态才用

$$x_{std} = \frac{x-\mu}{\sigma}$$

#### NLP

##### TF: Very low and very high term frequency (TF) values should be removed. 

Frequency measures can be used for vocabulary pruning to **remove** noise features by filtering the tokens with **very high and low** TF values across all the texts. Noise features are both the most frequent and most sparse (or rare) tokens in the dataset. On one end, noise features can be stop words that are typically present frequently in all the texts across the dataset. On the other end, noise features can be sparse terms that are present in only a few text files. Text classification involves dividing text documents into assigned classes. The frequent tokens strain the ML model to choose a decision boundary among the texts as the terms are present across all the texts (an example of underfitting). The rare tokens mislead the ML model into classifying texts containing the rare terms into a specific class (an example of overfitting). Thus, identifying and removing noise features are critical steps for text classification applications.

- **没用的词** 像介词什么的 **删去**；
- **TF特别小的词**，**删去**
- Keep those tokens that have intermediate frequency. 词频特别高和特别低都都被dropped了，**只留下了词频intermediate的**

##### Steps

Text preparation and wrangling step.

- **(Step 1)** Text Problem Formulation
- **(Step 2)** Data Curation （curation的意思是 检索）
    - The process of gathering relevant external text data via web services or web-spidering (scraping or crawling) programs that extract raw content from a source is known as data (text) curation
- **(Step 3)** Cleanse and Preparation
    - Regular Expression, Regex, delete HTML tags, Punctuation, Space, Numbers
    - Tokenisation: Split text into individual tokens.
    - Stemming 词干拆解
    - Remove Number: When numbers (or digits) are present in the text, they should be removed or substituted with the annotation “/number/.” 因为number通常为中性
    - Lemmatisation 词性还原: Lemmatisation **reduces the repetition of words** occurring in various forms while maintaining the semantic structure of the text data, thereby aiding in training less complex ML models.
    - 其中一步 Data Wrangling (Preprocessing)
        - Extraction: 得到新变量，e.g. calendar date
        - Aggregation: 合成相似的变量，e.g. wages + other incomes
        - Filtration: delete rows, etc. 
        - Conversion: Transform data type into uniformed one.

#### Confusion Matrix

| \                             | **Actual Training Result:** Class 1               | Actual Training Result: Class 0                  |
| ----------------------------- | ------------------------------------------------- | ------------------------------------------------ |
| Predicted Result: **Class 1** | **TP**: True Positive (Predicted Result - True)   | **FP**: False Positive (Predicted Result - True) |
| Predicted Result: **Class 0** | **FN**: False Negative (Predicted Result - False) | **TN**: True Negative                            |

- Precision: $P= \frac{TP}{TP+FP}$  ，predicted里面true的，**去真 Type I error**。因为分母为预测的都是真的的，分子为真的都是真的的。**分母都是prediction，分子是true actual的**
- Recall / Sensitivity: $ R = \frac{TP}{TP+FN}$  ，**纳伪 Type II error**。**分母都是Actual的，分子是true predict的**
- Accuracy: $A = \frac{TP+TN}{TP+FP+TN+FN}$  ， you get that
- F1 Score: $F1 = \frac{2}{1/P+1/R}$ ，第一行，第一列的调和平均。

F1 score is more appropriate (than accuracy) when there is unequal class distribution in the dataset and it is necessary to measure the equilibrium of precision and recall. 

#### Fitness

Overfitting: prediction error on the training dataset is small but on the cross-validation dataset is large.

That facts have three conclusions: (1) Overfitting, (2) high variance error, (3) slight regularisation 为此，可以考虑加入正则化项 L1 or L2 to constraint the number of weights, and avoid the overfitting.

Slight regularisation occurs when the prediction error on the training dataset is small, while the prediction error on the cross-validation data set is significantly larger. This difference in error is variance. High variance error, which typically is due to too many features and model complexity, results in model overfitting.

### Algorithm

- SVM - (1) Binary Target Variable, not continuous (2) no hyper-parameters
- CART (Classification and Regression Tree)
- LASSO Least Absolute Shrinkage and Selection Operator

#### Overfitting & Model Error

- **Data scientists express the trade-off between overfitting and generalization as a trade-off between cost** (the difference between in- and out-of-sample error rates) **and complexity**. They use the trade-off between cost and complexity to calibrate and visualize under- and overfitting and to optimize their models
  - Total in-sample errors (*E_in*) are generated by the predictions of the fitted relationship relative to actual target outcomes on the training sample. Total out-of-sample errors (*E_out*) are from either the validation or test samples. Low or no in-sample error but large out-of-sample error are indicative of poor generalization. 
  - Data scientists decompose the total out-of-sample error into three sources:
    1. **Bias error**, or the degree to which a model fits the training data. Algorithms with erroneous assumptions produce high bias with poor approximation, causing underfitting and high in-sample error.
    2. **Variance error**, or how much the model’s results change in response to new data from validation and test samples. Unstable models pick up noise and produce high variance, causing overfitting and high out-of-sample error.
    3. **Base error** due to randomness in the data.