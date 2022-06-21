Here I show how to rotate the histogram in the corner.corner() function so both histograms line up with the 2D distribution panel. 

Note that you will need to replace the core.py file in your corner site-packages with the one that I have in this directory for the histograms to rotate.

Also note that this is specifically designed for comparing two distributions. Using this core.py will rotate all histograms besides the i=0 (i.e., the top) histogram. Using this core.py file will work without error when comparing three or more distribtuions, but as stated will rotate all histograms except for the top one. 
