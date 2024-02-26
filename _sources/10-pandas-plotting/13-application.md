# Application

[Click here](https://colab.research.google.com/drive/1cOshaiEA5eHhJDOi22_x3GRHsxqC0L3_?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

All the materials to reproduce your work (notebook and data files, API call, etc) should be included in the assignment Google Drive folder.

## Question 1

**Q1A: Identify an aspect of your final project data (or another civic dataset) that you want to analyze. Answer to this question briefly describes the data you're working with and what aspects of it you want to analyze.**

**Q1B: Develop an outline for your data visualization workflow. This could be a list with bullet points, a narrative, or a visual diagram (or a combination of these elements). Answer to this question includes notes on a desired final data structure and preliminary outputs.**
- *NOTE: No code is required as part of this answer.*

**Q1C: Develop a Python program that uses Pandas plotting functions to generate at least three different plot types using your Q1A dataset and Q1B workflows. Answer to this question includes code + comments.**
- *I encourage folks to use this question to explore visualizations you might use for the final project.*

For each plot type (as appropriate), include the following elements or components:
- Title
- Axis labels
- Legend
- Scale or tickmarks
- Data source
 
Plot types to choose from:
- Line plots
- Bar chart
- Grouped bar chart
- Horizontal bar chart
- Stacked bar chart
- Histogram
- Box plot
- Area plot
- Scatter plot
- Pie chart
- Map

**Q1D: What challenges did you encounter? How did you approach solving them?**

## Question 2

**Q2A: Identify an aspect of your final project data (or another civic dataset) that you want to analyze. Answer to this question briefly describes the data you're working with and what aspects of it you want to analyze.**

**Q2B: Develop an outline for your data visualization workflow. This could be a list with bullet points, a narrative, or a visual diagram (or a combination of these elements). Answer to this question includes notes on a desired final data structure and preliminary outputs.**
- *NOTE: No code is required as part of this answer.*

**Q2C: Develop a Python program that uses Seaborn plotting functions to generate at least two different plot types. Answer to this question includes code + comments.**
- *I encourage folks to use this question to explore visualizations you might use for the final project.*

For each plot type (as appropriate), include the following elements or components:
- Title
- Axis labels
- Legend
- Scale or tickmarks
- Data source
 
Plot types to choose from:
- Line plots
- Bar chart
- Histogram
- Box plot
- Area plot
- Scatter plot

Remember in `seaborn` our way into these discrete plot types if via a few overarching functions based on what aspects of the data we want to highlight:
- `sns.replot()`
  * Shows relationships
  * Can be a scatterplot or line plot 
- `sns.lmplot()`
  * Visualizes linear models
  * Can include a combination of line plots and scatter plots
- `sns.displot()`
  * Shows value distribution
  *  Can include histograms or bar charts
- `sns.catplot()`
  * Shows category dimensions
  * Can include bar charts, box plots, violin plots 
  
**Q2D: What challenges did you encounter? How did you approach solving them?**