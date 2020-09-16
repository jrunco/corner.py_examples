Example of how to over-plot two corner plots using the corner.py python package.

Basic structure:
- Name the first corner.corner(), e.g. "example_fig". The 2nd corner.corner() must end with attaching it to the first corner.corner(): fig=example_fig


Parameters that need to be specified for every sample (i.e., every corner.corner() function):
- Bins must be specified for both samples. Specifying the bins for one sample does not carry over to the other sample.
- Parameters that specify appearance of the data such as fill_contours=True (smooths our 2-D parameter space), quantiles=[0.16, 0.5, 0.84] (puts dashed lines identifying these spots on the 1-D histogram), levels=(0, 1-np.exp(-0.5), 1-np.exp(-1.125), 1-np.exp(-2)) (specifies the #-sigma regions on the 2-D parameter space that are identified - in my example I point out the 1, 1.5, and 2-sigma regions [the default includes 0.5-sigma]).


Parameters that must be specified in the final corner.corner() function:
- The range must be specified in the plot of the second sample. Specifying the range in the first plot line does not work, as the plot will focus around the 2nd distribution.


Parameters that can be specified in either corner.corner() function:
- The x-axis and y-axis labels argument can go in either corner.corner() function.


Other information:
- show_titles=True can only show the median with uncertainties for one of the distributions in each 1-D histogram.  Use plt.text() to manually put in both if desired.


Lastly, note that I do not cover every in the detailed API documentation for the corner.corner() function.  
