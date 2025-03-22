# rubin_galplane_survey
This repository collects information on the Rubin Observatory's LSST survey in the Galactic Plane for coordination purposes

rubin_galplane_survey_footprint.json : HEALpixel map of the Rubin survey footprint in the Galactic Plane. The format should be self documenting, and the map
can be loaded as follows:

with open(output_file, 'r') as fin:
    jdata = json.load(fin)

The 'healpix_map' parameter contains an array of length 'n_healpix' (with the spatial resolution corresponding to the 'nside' specified).  The 'healpix_map' can be loaded into a numpy array and plotted accordingly. Values of 1 indicate HEALpixels within the survey footprint, with values of zero outside that region. 

rubin_galplane_survey_priority_footprint.json : HEALpixel map of the Rubin survey footprint including the scientific priority assigned to each HEALpixel.