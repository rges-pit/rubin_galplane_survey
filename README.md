# rubin_galplane_survey
This repository collects information on the Rubin Observatory's LSST survey in the Galactic 
Plane for coordination purposes

Full information on the Rubin Observatory's overall process for establishing its survey 
strategy can be found 
[on the Observatory's website](https://survey-strategy.lsst.io/index.html), 
and described in 
[Bianco et al. (2022)](https://iopscience.iop.org/article/10.3847/1538-4365/ac3e72). 

The footprint for the Rubin Galactic Plane Survey was based on recommendations from 
[Street et al. 2023](https://iopscience.iop.org/article/10.3847/1538-4365/acd6f4), and 
then further refined to ensure the footprint was contiguous.  The resulting footprint was 
published in the 
[Phase 3 Report from Rubin's Survey Cadence Optimization Committee](https://pstn-056.lsst.io/). 

Information on Rubin's Galactic Plane Survey footprint is provided in a machine-readable 
format in the file:

rubin_galplane_survey_footprint.json : HEALpixel map of the Rubin survey footprint in the Galactic Plane. The format should be self documenting, and the map
can be loaded as follows:

with open(output_file, 'r') as fin:
    jdata = json.load(fin)

The 'healpix_map' parameter contains an array of length 'n_healpix' (with the spatial resolution corresponding to the 'nside' specified).  The 'healpix_map' can be loaded into a numpy array and plotted accordingly. Values of 1 indicate HEALpixels within the survey footprint, with values of zero outside that region. 

Information is also provided on the priority of each HEALpixel for science, based on the 
overlap between the survey regions desired by multiple different science cases from the 
Rubin community.  More information can be found in [Street et al. 2023](https://iopscience.iop.org/article/10.3847/1538-4365/acd6f4).
rubin_galplane_survey_priority_footprint.json : HEALpixel map of the Rubin survey footprint including the scientific priority assigned to each HEALpixel.

The notebook rubin_galplane_survey_footprint.ipynb describes how to load and use the information 
in these files, as well as how to plot and rotate the HEALpixel data in the form of sky maps. 