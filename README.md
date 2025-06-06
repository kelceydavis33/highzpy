# highzpy
Library designed for processing and interpreting spectroscopic and photometric data from the James Webb Space Telescope

## Class Descriptions

### photometry_DataFrames:

Class of functions for loading in DataFrames from the photometry, designed for CEERS pipeline. No proprietary CEERS 
photometric files are included here.


get_color_table(dfi, obj = False): Generates a DataFrame of the colors that can be created with the input DataFrame photometry and assotiated 
            errors on those colors, reported through error propogation

            
load_photometry(path, photz_path, chi_path, zgrid_path, template_path, ignore_HST = True): Initializes a Pandas DataFrame with photometry information for given FITS files from both
            NIRCam pipeline reducations and EAZY photometric fitting outputs.

### SED_plotting:

Functions used for plotting Spectra Energy Distributions (SEDs) designed for CEERS photometry. Several 
    plotting functions are overly complicated (such as plot_em_all which will plot every single SED in a 
    DataFrame in a single plot). However, plots like get_sed and jon_plot are incredibly useful and staples of 
    high-z JWST papers.

