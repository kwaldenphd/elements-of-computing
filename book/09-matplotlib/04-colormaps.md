# Colormaps

As described by Kenneth Moreland, "One of the most fundamental features of scientific visualiation is the process of mapping scalar values to colors" (Moreland, "Diverging Color Maps for Scientific Visualization," in *Proceedings of the 5th International Symposium on Visual Computing*, December 2009. http://dx.doi.org/10.1007/978-3-642-10520-3_9)

The color scheme or pallette for a plot is most often referred to as a colormap. Colormaps generally fall into a few categories, and `matplotlib` includes [a wide range of built-in colormaps](https://matplotlib.org/stable/tutorials/colors/colormaps.html), some of which are shown in the images below.

## Sequential

<p align="center"><img class="aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch10/fig2.png?raw=true" /></a></p>

Sequential colormaps show change in lightness or color saturation incrementally. They are generally comprised of a single hue.

## Diverging

<p align="center"><img class="aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch9/fig3.png?raw=true" /></a></p>

Diverging colormaps show change in lightness and possibly saturation for two different colors that meet in the middle at an unsaturated color. This type of colormap is most effective when data being plotted has a critical middle value, or deviates around zero.

## Cyclic

<p align="center"><img class="aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch9/fig4.png?raw=true" /></a></p>

Cyclic colormaps show change in lightness for two different colors that meet in the middle and begin or end at an unsaturated color. This type of colormap is most effective for data values that wrap around at the endpoints (i.e. phase angle, wind direction, time of day).

## Qualitative

<p align="center"><img class="aligncenter" src="https://github.com/kwaldenphd/elements-of-computing/blob/main/book/images/ch9/fig5.png?raw=true" /></a></p>

Qualitative colormaps are miscellaneous colors. This type of colormap is most effective for information that does not have ordering or relationships.

## Additional Resources

For more on colormaps in `matplotlib`:
- [Colormaps](https://matplotlib.org/stable/tutorials/colors/colormaps.html)
- [Choosing Colormaps in Matplotlib](https://matplotlib.org/stable/tutorials/colors/colormaps.htm9
- [Creating Colormaps in Matplotlib](https://matplotlib.org/stable/tutorials/colors/colormap-manipulation.html)