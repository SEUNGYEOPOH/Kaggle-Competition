# Binary Classification of Insurance Cross Selling

## Our team
<div align="center">
<table width="950">
    <thead>
    </thead>
    <tbody>
    <tr>
        <th>Profile</th>
         <td width="100" align="center">
              <a href="https://seungyeopoh.github.io/CV/">
                CV
            </a>
        </td>
        <td width="100" align="center">
<!--            <a href="https://github.com/"> -->
<!--                 test -->
            </a>
        </td>
    </tr>
    <tr>
        <th>Name</th>
        <td width="100" align="center">오승엽</td>
        <td width="100" align="center">박윤서</td>
    </tr>
    <tr>
        <th>GitHub</th>
        <td width="100" align="center">
            <a href="https://github.com/SEUNGYEOPOH">
                <img src="http://img.shields.io/badge/SEUNGYEOPOH-green?style=social&logo=github"/>
            </a>
        </td>
        <td width="100" align="center">
            <a href="https://github.com/Gangsui">
                <img src="http://img.shields.io/badge/Gangsui-green?style=social&logo=github"/>
            </a>
        </td>
    </tr>
    </tbody>
</table>
</div>

## Data Preprocessing
- Factorize categorical variables with low correlation and continuous variables with high correlation
    - Additional expansion of 4 features
- Feature Engineering: Continuous and categorical features were separated. Categorical features were encoded using an Ordinal Encoder.

## Modeling
- LGBM
  - Bayesian optimization
  - SMOTE
  - Remove outliar
- Xgboost
  - Bayesian optimization
- Catboost
  - Bayesian optimization
  - Optimization based on number of categorical variables
- DNN
  - Drop-Out
  - Class weight
  - Over Sampling
    
Neural Network Model
The Neural Network was designed to effectively handle both continuous and categorical features:

- Categorical Features:

   - Embedding Layers: Categorical features were processed using embedding layers. This approach was chosen to avoid the inefficiencies of one-hot encoding, which can lead to sparse data with many zeros, causing unnecessary computations in a Deep Neural Network (DNN). By using embeddings, the model can learn compact, dense representations of categorical variables, capturing relationships and patterns within the data, such as similarities between regions (Region_Code), vehicle age (Vehicle_Age), and sales channels (Policy_Sales_Channel).
     
- Continuous Features: These were combined with the flattened embeddings of categorical features to form the input to the subsequent layers of the network, allowing the model to learn from both types of data simultaneously.

- Model Architecture: The network architecture consists of dense layers activated by the Mish function, which is known for its smooth, non-monotonic nature, helping the model to learn complex patterns. Batch Normalization was applied to improve training stability, reduce overfitting, and accelerate convergence.

- Output Layer: A sigmoid activation function was used in the output layer, suitable for binary classification tasks, to produce probabilities indicating the likelihood of each class.

## Result
- Evaluation : ROC Curve
- Public Score : 0.89585
- Private Score : 0.89562
- top 12.9% based on private score
