# Application

[Click here](https://colab.research.google.com/drive/1Oz7GGpg5jqchdPTk7_4IrYKf8EuyDoM-?usp=sharing) for a Jupyter Notebook template for this chapter's application problems.

## Submitting Additional Data Files 

- Option #1: Upload the additional files as part of the Canvas submission
  * If working in Google Docs and submitting a link, you’ll need a second submission for the file.
- Option #2: Put any CSV or JSON files in Google Drive and/or import to Google Sheets, check sharing permissions, and submit the URL.
  * This may require a second Canvas submission.
- Option #3: Put materials (Google Doc, Colab link, data file) in a Google Drive folder, check sharing permissions, and submit the URL on Canvas.

## Question 1

**Q1A: Identify a civic dataset that you want to analyze. Answer to this question notes and briefly describes the dataset you're working with. Include a link if possible.**
- *I encourage folks to use this question to explore civic data you might use for the final project.*

**Q1B: Develop an outline for your data visualization workflow. This could be a list with bullet points, a narrative, or a visual diagram (or a combination of these elements). Answer to this question includes a desired final data structure.**
- *NOTE: No code is required as part of this answer.*

**Q1C: Develop a Python program that uses Pandas plotting functions to generate at least three different plot types. Answer to this question includes code + comments.**
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

**Q2A: Identify a civic dataset that you want to analyze. Answer to this question notes and briefly describes the dataset you're working with. Include a link if possible.**
- *I encourage folks to use this question to explore civic data you might use for the final project.*

**Q2B: Develop an outline for your data visualization workflow. This could be a list with bullet points, a narrative, or a visual diagram (or a combination of these elements). Answer to this question includes a desired final data structure.**
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