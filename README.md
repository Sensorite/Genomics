Importing necessary libraries:
pandas for data manipulation
sklearn for t-SNE dimensionality reduction
mpl_toolkits.mplot3d for 3D plotting
matplotlib.pyplot for visualization
Loading data from CSV file 'medulloblastoma_data.csv' using pd.read_csv function
Selecting relevant columns using df[['MB_subgroup', 'TP53_status', 'MYC_status', 'Age_years']] syntax
Converting categorical variables to dummy variables using pd.get_dummies function
Applying t-SNE to the data using TSNE class from sklearn.manifold module:
Specifying n_components=3 to reduce the data to 3 dimensions
Specifying perplexity=10 to control the trade-off between preserving local vs global structure of the data
Creating a 3D scatter plot of the t-SNE data using plt.scatter function:
Using tsne_data[:, 0], tsne_data[:, 1], and tsne_data[:, 2] to represent t-SNE dimensions 1, 2, and 3, respectively
Coloring the points by the 'MB_subgroup' column using the c=df['MB_subgroup'] argument
Specifying the 'viridis' colormap using cmap='viridis'
Saving the t-SNE data to a CSV file called 'medulloblastoma_tsne.csv' using pd.DataFrame constructor and the to_csv method
The resulting CSV file can be imported into RStudio for further analysis and visualization.
