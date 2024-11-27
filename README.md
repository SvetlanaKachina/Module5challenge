# Module5challenge
While preparing the Data, we ran the provided package dependency and data imports, and then merged the mouse_metadata and study_results DataFrames into a single DataFrame.

We found out that MouseID “g989” has duplicate time points. After displaying the data associated with that mouse ID, we then created a new DataFrame where this data is removed. DataFrame with dropped duplicate Mouse ID was used going further.

We then display the updated number of unique mice IDs in cleaned_study_complete.

Generating Summary Statistics
Before creating a DataFrame of summary statistics, we declared everything we’d be looking to work with: 
-means
-medians
- variances
-stds(standard deviations)
-sems.
Our summary statistics table (stats_table) includes:

*a row for each drug regimen. 
*a column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.(we used groupby and.agg for that)

Bar Charts and Pie Charts
We generated two bar charts. Both charts are identical and show the total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

We created the first bar chart with the Pandas DataFrame.plot() method.

We created the second bar chart with Matplotlib's pyplot methods.

We, then, generated two pie charts. Both charts are identical and show the distribution of unique female versus male mice in the study.

We created the first pie chart with the Pandas DataFrame.plot() method.(we have done a separate mouse_sex_df first, then used value_counts)

We created the second pie chart with Matplotlib's pyplot methods.

Quartiles, Find Outliers, and Create a Box Plot

We calculated the final tumor volume (using “merge”) of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, we calculated the quartiles and IQR, and determine if there are any potential outliers across all four treatment regimens(using groupby, reset_index and merge). 

We then created a Line Plot and a Scatter Plot

Selected a single mouse that was treated with Capomulin, and generated a line plot of tumor volume versus time point for that mouse.

Generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

Calculated Correlation and Regression
Calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

Plotted the linear regression model on top of the previous scatter plot.


Analyzing received graphs, charts and box plot, we can conclude on a few things that require our attention:
1. Capomulin is clearly working based on the linear graph for mouse l509.
2. Relationship between the weight of the mice and it’s tumor size is shown on the scatter plot graph, and is something to be considered, perhaps, for the new series of tests. As we can observe, the more the weight of the mice, the larger their tumor volumes. The same conclusion will show us Lenear regression graph.
3. Box plot shows that although we have 1 outlier, , for the most parts 2 different drugs were used to treat Tumor Volumes of approximately 20 – 50 mm3 (Capomulin and Ramicane) and another two drugs, Ifubinol and Ceftamin were used to treat Tumor Volume above 50 mm3. We have seen that Capomulin is clearly working (in the liner graph above), we suggest creating comparative analysis between those drugs for the both sized sections in order to determine which drug is more affective prior to going further.
As different sized tumors in our set are being treated with different drugs, there won’t be a single drug for us to proceed in our further studies, rather 1 drug from each of two groups. 
