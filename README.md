# Vehicle Price Classification (ANN)

Multi-Layer Perceptron (MLP) model developed to classify used vehicles into five price categories based on market specifications. 

## Performance Summary
The model was optimized to achieve a 5.35% increase in average accuracy over the baseline, satisfying the performance requirements needed.

| Model | Avg. Accuracy | Avg. Cross-Entropy Loss |
| :--- | :--- | :--- |
| Baseline  | 84.52% | 0.4023  |
| Optimized | 89.87% | 0.2811  |

## Model Architecture
* **Hidden Layers**: Dual-layer structure with 160 and 80 neurons respectively.
* **Activation Function**: ReLU (Rectified Linear Unit).
* **Optimization**: Adam solver utilizing a tuned learning rate of 0.0005.
* **Validation Strategy**: 10-fold cross-validation implemented to verify statistical stability across all data subsets.

## Data Pipeline
* **Outlier Handling**: Removal of price and mileage anomalies to maintain clean decision boundaries.
* **Feature Engineering**: Integration of high-cardinality categorical attributes including Manufacturer and Fuel Type.
* **Normalization**: Min-Max scaling of continuous variables to the [0, 1] range.
* **Categorization**: Discretization of the continuous price target into five equal-width intervals via pd.cut.

## Technical Stack
* Python 3.x
* Scikit-Learn
* Pandas
* NumPy
