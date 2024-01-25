# Introduction to `plotly`

"Plotly is a technical computing company headquartered in Montreal, Quebec, that develops online data analytics and visualization tools. Plotly provides online graphing, analytics, and statistics tools for individuals and collaboration, as well as scientific graphing libraries for Python, R, MATLAB, Perl, Julia, Arduino, and REST" ([Wikipedia](https://en.wikipedia.org/wiki/Plotly)).

The `plotly` Python graphing library is supported by the Plotly company. Plotly relies on Python and the Django framework, using JavaScript, D3.js, HTML, and CSS for its front-end. Plotly files are stored on Amazon Web Services' Simple Storage Service (S3). The company was founded in 2012 and went on to be a featured startup at 2013 PyCon, sponsoring the SciPy conference in 2018. During Series A funding, Plotly raised $5.5 million, supported by MHS Capital, Siemens Venture Capital, Rho Ventures, Real Ventures, and Silicon Valley Bank.

Plotly offers a range of products, some of which are free or open-source, and others that are subscription based.
- ***Dash***: an open-source web application framework for Python, R, and Julia
- ***Chart Studio***: a graphical user interface for analyzing and visualizing data; single-user version is free, enterprise deployments have a pricing model
- ***API libraries***: open-source graphing libraries for Python, R, and Julia
- ***Plotly Apps***: Google Chrome app
- ***PLotly.js***: open-source JavaScript graphic and dashboard library
- ***Plotly Enterprise***: pricing model for local Plotly installation and deployment

In recent years, Plotly has moved into machine learning and artificial intelligence app support and artificial intelligence supply chain technology and continues to expand its enterprise pricing options. 
- For more on Plotly history: [Plotly, "About Us"](https://plotly.com/about-us/)
- For more on Plotly products:
  - [Dash Enterprise](https://plotly.com/dash/)
  - [Consulting and Training](https://plotly.com/consulting-and-oem/)
  - [Chart Studio](https://plotly.com/chart-studio/)

Plotly's enterprise products are used by corporations that include NVIDIA, Tesla, Shell, Citi Bank, and Amgen. Plotly's Chart Studio product is used by a range of journalism outfits and companies, including S&P Global, The Washington Post, Wired, Tesla, and Medium.

## Installing `plotly` 

To install `plotly`:
- using `pip`: `pip install plotly`
- using `conda`: `conda install -c plotly`

A couple Jupyter-notebook specific installs:
- using Jupyter Notebook: `pip install "notebook>=5.3" "ipywidgets>=7.2"`
- using `conda` in Jupyter Notebook: `conda install "notebook>=5.3" "ipywidgets>=7.2"`
