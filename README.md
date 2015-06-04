# A0620-00 SMARTS Optical Photometry
optical light curves for SMARTS data on the X-Ray Binary source A0620-00

This repository contains photometry provided by Andy Cantrell and Rachel MacDonald on SMARTS observations taken from about 2003-2008

Michelle Buxton also has photometry on A0620-00 from about 2013-2015, but it is using different comparison stars. The data are not here, but can be accessed at http://www.astro.yale.edu/smarts/xrb/tables/A0620-00.tab. There is some code in the ipython notebook in this repository I wrote that fetches the table and reads in the B, V, and I photometry into pandas data frames.

It also contains photometry I calculated on SMARTS observations takne from 2009-2015, in an attempt to catch up on the data.
I made two csv files with photometry for each filter. one where I use the same comparison stars as Andy and Rachel (A0620_AC_{B,V,I}.csv), and the other using Michelle's comparison stars (A0620_{B,V,I}.csv).

In the IPython notebook you will find routines for aligning the fits images in different bands, pyraf code to preform the photometry, and some python code to read in the output of the photometry files to pandas data frames, do some data cleaning, and calibrations on the data to get it to the true magnitude scale.

The FITS images and the photometry files are not in this repository. The total number of photometry and FITS files would be around 5000 files, and not feesible. However, the FITS images are accessible on the SMARTS FTP site, and can be downloaded there. Once the FITS files are obtained, one can use the code in this IPython notebook to reproduce these results. Send me an email if you are interested. 


Dependencies
------------
To do absolutely everything in this notebook, you need  the following python packages : [astropy](http://www.astropy.org/), [alipy](http://obswww.unige.ch/~tewes/alipy/index.html), [pyfits3](http://www.stsci.edu/institute/software_hardware/pyfits/), [pyraf](http://www.stsci.edu/institute/software_hardware/pyraf), [numpy](http://www.numpy.org/), [pandas](http://pandas.pydata.org/), and [asciidata](http://www.stecf.org/software/PYTHONtools/astroasciidata/), and their dependencies therein. These are all open source python packages so you can download them to your system, although most come with the conda distribution.

There are also some instructional sections in the IPython notebook that refer to [IRAF](http://iraf.noao.edu/), and [SOA Image DS9](http://ds9.si.edu/site/Download.html)

If you just want to use the code to mess around with the ascii data, you just need pandas and numpy
