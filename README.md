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
- 

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

## Result
- Evaluation : ROC Curve
- Public Score : 0.89585
- Private Score : 0.89562
- top 12.9% based on private score
