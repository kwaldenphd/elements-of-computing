# Essential Visualization Elements

When building data visualizations, it is useful to keep in mind the core elements needed for a visualization to be legible, accessible, and meaningful.

The following elements can appear in a data visualization via a wide range of design options:
- Title and subtitle
- Axis labels
- Coordinate system
- Scale
- Legend
- Source information

It is also critically important to make sure the visualization will be accessible to the widest range of possible users. Prioritizing accessibility shapes color choices and visual style options, but also underscores the need to have a deep grasp on what you are trying to accomplish in a visualization.

Some of the questions to consider include...
- Is your visualization's color scheme/pallete/map accessible for individuals with color blindness?
- Are your visualization's color components or other visual cues going to be legible in the final publishing medium or format? 
  * For example, you may have a visualization that is readable on a large projection screen but not on letter-size paper.
- Can someone interacting with your visualization easily access the data driving the visualization? 
  * In situations where you are working with proprietary, sensitive, or licensed data, providing the full back-end dataset may not always be possible.
  * At the very minimum, a citation to the data source is needed.
  * When possible, document the steps taken and changes made to the data from its original form in the process generating the visualization
  * The gold standard here is reproducibility, with code/scripts and data available to end users
- Is the visualization the only way or place this information is communicated?
  * Imagine a situation where a visually impaired person is interacting with your visualization. 
  * Having multiple points of entry or forms of representation for the information contained in the visualization ensures this information is available to the widest possible range of users.

Things like alt text, plain-text tables, captions, narrative text, etc. can all help improve the accessibility of data visualizations. Axis Maps's [Colorbrewer2.0](https://colorbrewer2.org/) is a useful tool for finding accessible color palletes.