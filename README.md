# corner_examples
Example of how to over-plot two corner plots using the corner.py python package.

- Bins must be specified for both samples. Specifying the bins for one sample does not carry over to the other sample.
- The range must be specified in the plot of the second sample. Specifying the range in the first plot line does not work, as the plot will focus around the 2nd distribution.


- Name the first corner.corner(), e.g. "example_fig". The 2nd corner.corner() must end with attaching it to the first corner.corner(): fig=example_fig
