# Quantitative mapping of cerebrovascular reactivity amplitude and delay with breath-hold BOLD fMRI when end-tidal CO<sub>2</sub> quality is low
This analysis code is being shared to accompany the manuscript available here: https://www.biorxiv.org/content/10.1101/2024.11.18.624159v1

# Code (More to Come)

`Get_CO2_increases.py` contains functions that can be used to classify breath holds in a CO₂ timeseries as high-quality based on the CO₂ change they induce. This can provide information about a participant's compliance during a breath hold task. We recommend using the functions in the following order:

1. Use `get_BH_locations()` to identify the start and end locations of each breath-hold in an exhaled CO₂ timeseries and plot the timeseries with marked breath-hold periods for manual verification.
2. After manually verifying that the outputted start and end locations are correct, use `get_BH_CO2_increases()` to calculate the CO₂ increase associated with each breath hold. 
3. Decide on a threshold to classify breath holds as "high-quality," and then use `check_BH_quality()` to output a binary array that is as long as the number of breath holds, with 1s corresponding to each high-quality breath hold and 0s elsewhere.


