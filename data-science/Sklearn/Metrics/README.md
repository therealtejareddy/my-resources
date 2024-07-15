### Classification metrics
| Metric | Description | 
| --- | --- | 
 Accuracy | Ratio of correct predictions to total predictions 
 Precision | True Positive over all positive predictions
 Recall | True Positive over all actual positives
F1-Score | Harmonic mean of precision and recall
AUC-ROC | Models ability to distinguish between classes
---

- `Accuracy = ( TP+TN  ) / ( TP+TN+FP+FN )` 
- `Precision = TP / ( TP+FP )`
- `Recall = TP / TP + FN`
- `F1-Score = 2× ( ( Precision * Recall ) / ( Precision + Recall ) ) `


- **TP (True Positives)**      : The number of correctly predicted positive instances.
- **TN (True Negatives)**   : The number of correctly predicted negative instances.
- **FP (False Positives)**    : The number of incorrectly predicted positive instances.
- **FN (False Negatives)** : The number of incorrectly predicted negative instances.

```python
from sklearn.metrics import confusion_matrix,accuracy_score,precision_score,recall_score,f1_score,roc_curve,auc

y_true = [0, 1, 1, 0, 1, 0, 0, 1, 1, 0]   
# Predicted labels 
y_pred = [0, 1, 0, 0, 1, 1, 0, 1, 1, 1] 


# Confusion Matrix 
cm = confusion_matrix(y_true, y_pred) 
# Accuracy 
accuracy = accuracy_score(y_true, y_pred) 
# Precision 
precision = precision_score(y_true, y_pred) 
# Recall 
recall = recall_score(y_true, y_pred) 
# F1-Score 
f1 = f1_score(y_true, y_pred) 
# ROC Curve and AUC 
fpr, tpr, thresholds = roc_curve(y_true, y_pred) 
roc_auc = auc(fpr, tpr) 
  
print("Confusion Matrix:") 
print(cm) 
print("Accuracy:", accuracy) 
print("Precision:", precision) 
print("Recall:", recall) 
print("F1-Score:", f1) 
print("ROC AUC:", roc_auc) 
```

### Regression Metrics
| Metric | Description | 
| --- | --- | 
 MAE | Average absolute difference between predicted and true
 MSE | Average squared difference between predicted and true
 RMSE | Square root of MSE
Log Loss | Loss based on probability estimates
 R - squared | Variance explained by the model
---

```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score

mae = mean_absolute_error(Y_true, Y_predict)
print("Mean Absolute Error:", mae)

mse = mean_squared_error(Y_true, Y_predict)
print("Mean Squared Error:", mse)

r2s = r2_score(Y_true, Y_predict)
print("R Squared Score:", r2s)

rmse = np.sqrt(mse)
print("Root Mean Squared Error:", rmse)
```