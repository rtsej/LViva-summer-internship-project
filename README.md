# Labviva 2024 Summer Project Summary
This project focuses on enhancing Labviva's platform by developing predictive models to estimate shipment and delivery times for life science laboratory products. Accurate delivery predictions are critical for customer confidence and decision-making, allowing buyers to compare products based on both availability and delivery timelines.
## Objectives
- Develop predictive models to estimate shipping times using internal data sources
- Establish a robust data pipeline to extract and prepare the necessary data for modeling
- Conduct exploratory data analysis (EDA) to identify meaningful patterns and correlations.
- Build and evaluate baseline models to guide future advanced modeling efforts
## Approach
### Data Integration:
- Data was sourced from three internal tables describing different data elements
- Complex cross-referencing using key identifiers was used to link records across tables
- Result: a unified dataset containing essential features and relevant metadata
### Data Cleaning and Feature Engineering:
- Cleaned invalid entries (e.g., negative shipping times, missing values)
- Created a feature to serve as the primary target variable describing an element of delivery time
- Extracted additional features to capture potentially important seasonal trends. Considered cyclic transformations to better represent time-based patterns.
### Exploratory Data Analysis (EDA):
- Investigated potential correlations between shipping time and various features 
- Visualized relationships to identify trends and outliers, noting limitations due to the small dataset size
- Highlighted potential biases in the dataset 
### Model Development:
- Split the data into training and testing sets using a 67/33 ratio
- Built baseline models:
  - Linear Regression: Explored linear relationships between features and shipping time
  - Random Forest Regressor: Captured potential non-linear relationships in the data
- Observed high mean squared errors (MSE) due to the limited dataset, with values exceeding acceptable thresholds for practical applications
## Results
- Despite promising initial correlations, the dataset's small size limited the reliability of the results
- Early models provided a baseline for comparison but highlighted the need for more comprehensive data to improve accuracy
## Challenges
- Dataset Size
- Data Integration
- Limited Feature Representation
## Recommendations for Future Work
- Data Expansion:
  - Implement data integrity checks at acquisition to prevent issues like invalid dates and missing values.
  - Capture additional attributes to enhance feature richness.
- Feature Engineering:
  - Convert date-based features into cyclic representations for improved seasonal trend modeling
  - Introduce engineered features
- Advanced Modeling:
  - Revisit EDA and model baselines with expanded data
  - Explore more sophisticated models, such as gradient boosting or neural networks, to capture complex relationships
  - Establish separate test sets for hyperparameter tuning and unbiased evaluation.
## Technical Tools Used
- Programming Language: Python
- Libraries Used:
  - pandas and numpy for data cleaning and manipulation
  - sklearn for train-test splitting and baseline model development
- Visualization libraries for EDA (matplotlib)
- Data Management: Dataset preparation and integration were performed in a Jupyter Notebook 


## Future Impact
Once refined, these models will enable Labviva to provide accurate shipping estimates, improving customer trust and streamlining supplier management.
