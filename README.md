Below I outline how to format multiple corner.corner() functions and corresponding parameters in the functions to display multiple distributions in one corner.py plot. This is meant to be supplemental information to go along with the python example in this repository.

I do not go over the basics of how to use the corner.corner() function, see the official 
<a href="https://corner.readthedocs.io/en/latest/index.html">Corner.py</a> website for that information.
**Important disclaimer: I am not the creator of corner.py and do not claim any ownership over its maintenance.**

1. Basic structure:
   - One corner.corner() function is needed for every data set
   - Name the first corner.corner(), e.g. "example_fig". The 2nd corner.corner() must end with attaching it to the first corner.corner(): fig=example_fig

2. Parameter formatting
   - Parameters that modify the appearance of individual data sets must be specified in ever corner.corner() function. Specifying these parameters in the first corner.corner() function does not carry over to subsequent corner.corner() functions.  Examples of parameters that this applies to are:
      - **bins**
      - **color**
      - **fill_contours**
      - **quantiles**
      - **hist_kwargs**
   - Some parameters must be specified in a specific corner.corner() function:
      - **range** must be specified in the final corner.corner() function. Specifying the range in the first corner.corner() function does not work, as the plot window will focus around the 2nd distribution.
   - Some parameters can be specified in any corner.corner() function. These parameters only need to be specified once, and the appearance of the plot will not change based on which corner.corner() function they are included in:
      - **labels**The x-axis and y-axis labels argument can go in either corner.corner() function.

3. Other information:
   - **show_titles**=True can only show the median with uncertainties for one of the distributions in each 1-D histogram.  Use plt.text() to manually put in both if desired.

Lastly, note that I do not discuss how to use every parameter available in the <a href="https://corner.readthedocs.io/en/latest/api.html">detailed API documentation</a> for the corner.corner() function. I limit my discussion above to the parameters that are used in the corner example in this repository.
