This Python notebook, titled "Handling_Outliers.ipynb," demonstrates how to handle outliers in a dataset, specifically using an Uber fares dataset. The key steps involved are:

1. **Data Preparation**: 
   - The notebook starts by downloading and extracting the Uber dataset.
   - Unnecessary columns like pickup/dropoff longitude and latitude are dropped to simplify the dataset.

2. **Exploratory Data Analysis (EDA)**:
   - The dataset is analyzed using the `describe()` function to observe statistical information.
   - Histograms and box plots are used to visualize the distribution of the fare amounts, showing that the data is left-skewed and not normally distributed.

3. **Outlier Detection**:
   - The interquartile range (IQR) method is used to detect outliers in the fare amount and passenger count. A custom function is created to find and summarize these outliers.
   
4. **Handling Outliers**:
   - Instead of removing outliers, the notebook demonstrates **capping** them by setting upper and lower limits based on the mean and standard deviation (3 standard deviations from the mean).
   - `np.where()` is used to replace values beyond these limits with the capped values.

5. **Results**:
   - After capping the outliers, the distribution of the data is closer to normal, making it suitable for further analysis.

The notebook provides a clear example of how to handle outliers in real-world datasets using IQR and capping techniques to avoid negatively impacting the data.
