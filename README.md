# Matplotlib Challenge

Data analysis of an animal study, which was conducted to compare the performance of treatment regimens for mice identified with squamous cell carcinoma (SCC) tumor growth. Used the pandas library and matplotlib library to generate tables and figures that better help us understand and visualize those study results.

* [Background](#background)
* [Observations and Insights](#insights)
* [Jupyter Notebook](#nb)
* [Images](#images)
* [Technologies Used](#technologies)

##  <a name="background"></a>Background

For this project, I started with 2 csv files. Both of these files can be found [here](./data). One [csv file](./data/Study_results.csv) includes the study results for each mouse that took part in the study. It includes columns for mouse id, timepoint, tumor volume, and metastatic sites.  The other [csv file](./data/Mouse_metadata.csv) includes metadata information about the mice that participated in this study, such as mouse id, drug regimen, sex, age, and weight. For this analysis, I loaded the two csv files into pandas dataframes. I merged these two dataframes based on the mouse id field they share to create a combined dataframe. I used the combined dataframe along with the pandas and matplotlib libraries to help generate the various tables and graphs needed to understand the results.

## <a name="insights"></a>Observations and Insights

Observations or inferences that can be made from the data.

* There's a strong, positive correlation between average weight (g) and tumor volume (mm3) for mice treated with the Capomulin drug regimen. That is, as the weight of a mouse increases, the tumor volume increases as well. Both of these variables move in the same direction with generally the same magnitude.

* The distribution of female and male mice was roughly the same for this study. So, gender is generally not a factor in average weight or average tumor volume. That is, the results of this study are applicable to both male and female mice.

* The box and whisker plots show the final tumor volume (mm3) for mice treated with the most promising regimens. From those plots, we can see that Capomulin and Ramicane had considerably lower median final tumor volume as compared to Infubinol and Ceftamin. So, it looks like Capomulin and Ramicane are the most effective drug regimens for reducing tumor sizes.

* However, even though the box plots show smaller median values for Capomulin and Ramicane, the bar plots show that these two drug regimens had considerably more data points than the other drug regimens. Perhaps, if the number of data points were more equal among the different drug regimens, then maybe the median final tumor sizes would be more or less the same.

* From the data, we plotted (as a line graph) the tumor volume (mm3) over time for mouse s185 (which was treated with Capomulin). From this visualization, we can see that the tumor volume for mouse s185 decreased steadily over time. If we were to plot other mice treated with Capomulin, it would be interesting to see if there is a similar relationship between tumor volume and time.

* As shown in the box and whisker plots, there is only one considerable outlier for the Infubinol drug regimen. This is significant to note because we are less likely to have distorted results as much of the data for the different regimens is within the upper and lower bounds

##  <a name="nb"></a>Jupyter Notebook

For this project, I used jupyter notebook to render and display the results of this analysis. You can view the notebook here:

<https://nbviewer.jupyter.org/github/philipstubbs13/matplotlib-challenge/blob/master/pymaceuticals.ipynb>

The notebook is also available inside this repository [here](./pymaceuticals.ipynb).

In this notebook, you will find the following:

* [Summary Statistics](#summary_statistics)
* [Bar Plots](#bar_plots)
* [Pie Plots](#pie_plots)
* [Quartiles, Outliers, and Boxplots](#box_plots)
* [Line and Scatter Plots](#line_plot)

### <a name="summary_statistics"></a>Summary Statistics

* The summary statistics (in tabular format) consist of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

### <a name="bar_plots"></a>Bar Plots

* The bar plots show the number of data points for each treatment regimen. One plot is built using the pandas library and the other is built using the matplotlib library. Besides that difference, they are the exactly the same plot.

### <a name="pie_plots"></a>Pie Plots

* The pie plots chart the distribution of female versus male mice in the study. One plot is built using the pandas library and the other is built using the matplotlib library. Besides that difference, they are the exactly the same plot.

### <a name="box_plots"></a>Quartiles, Outliers, and Boxplots

* To generate the box plots, the final tumor volume of each mouse across four of the most promising treatment regimens (Capomulin, Ramicane, Infubinol, and Ceftamin) was calculated. Then, the quartiles and IQR were calculated to help determine if there are any potential outliers across all four treatment regimens.
* The box and whisker plot shows the final tumor volume for all four treatment regimens (on the same plot) and highlights potential outliers (represented as a blue dot on the plot).

### <a name="line_plot"></a> Line and Scatter Plots

* A line plot was generated to show time point versus tumor volume for mouse s185. The mouse was treated with Capomulin.
* A scatter plot was created to show average mouse weight versus average tumor volume for the Capomulin treatment regimen.
* Finally, the correlation coefficient and linear regression model between average mouse weight and average tumor volume for the Capomulin treatment were calculated. The linear regression model is plotted on top of the scatter plot.

##  <a name="nb"></a>Images

* Static images of the different visualizations can be found [here](./Images).

##  <a name="technologies"></a>Technologies Used

* Python
* Pandas library
* Jupyter Notebook
* Matplotlib library