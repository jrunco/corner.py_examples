Example of how to over-plot two corner plots using the corner.py python package.

Below I outline how to format the parameters of the corner.corner() function to display multiple distributions in one corner.py plot.
I do not go over the basics of how to use the corner.corner() function, see the official 
<a href="https://corner.readthedocs.io/en/latest/index.html">Corner.py</a> website, which I am not the creator of, for that information.
Important disclaimer: I am not the creator of corner.py and do not claim any ownership over its maitanance. 

Basic structure:
- One corner.corner() function is needed for every distribution of data
- Name the first corner.corner(), e.g. "example_fig". The 2nd corner.corner() must end with attaching it to the first corner.corner(): fig=example_fig


Parameters that need to be specified for every sample (i.e., every corner.corner() function). Specifying these parameters for one sample does not carry over to the other sample:
- bins 
- fill_contours (e.g. fill_contours=True)
- quantiles=[0.16, 0.5, 0.84] (puts dashed lines identifying these spots on the 1-D histogram)
- levels=(0, 1-np.exp(-0.5), 1-np.exp(-1.125), 1-np.exp(-2)) (specifies the #-sigma regions on the 2-D parameter space that are identified 


Parameters that must be specified in the final corner.corner() function:
- The range must be specified in the plot of the second sample. Specifying the range in the first plot line does not work, as the plot will focus around the 2nd distribution.


Parameters that can be specified in either corner.corner() function:
- The x-axis and y-axis labels argument can go in either corner.corner() function.


Other information:
- show_titles=True can only show the median with uncertainties for one of the distributions in each 1-D histogram.  Use plt.text() to manually put in both if desired.


Lastly, note that I do not cover every in the detailed API documentation for the corner.corner() function.  
