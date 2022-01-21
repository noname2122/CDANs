# CDANs - Causal Discovery from Autocorrelated and Non-Stationary Data

## Organization of the files and folders
1. The datasets used in the experiments are located in the "data" directory
    a.  synthetic_data.csv - Contains the synthetic data generated for the experiments
    b.  ot_conservative.csv - Contains the oxygenation parameters and ventilator settings for the conservative oxygen therapy treatment
    c.  ot_conservative.csv - Contains the oxygenation parameters and ventilator settings for the liberal oxygen therapy treatment
3. The code used to run the experiments are located in the "code" directory
    a. get_lagged_links.ipynb - A Python Jupyter notebook to estimated the lagged and autocorrelated causal relationships.
    b. synthetic_data.mlx - A Matlab script that estimates the contemporaneous causal relationships and changing modules for *Synthetic Data* using the lagged relationships estimated in 3(a).
    c. ot_conservative.mlx - A Matlab script that estimates the contemporaneous causal relationships and changing modules for *Conservative Oxygen Therapy* using the lagged relationships estimated in 3(a).
    d. ot_liberal.mlx - A Matlab script that estimates the contemporaneous causal relationships and changing modules for *Liberal Oxygen Therapy* using the lagged relationships estimated in 3(a).

## How to run the code and obtain the results

# Step 1: 
To get the lagged and autocorrelated causal links, you need to run get_lagged_links in python/colab and save the output links. You can use any datasets included in the data folder and change the file names in the code.
# Step 2: 
After getting the lagged and autocorrelated causal links, you need to generate new variables (shifted variables of the original one to feed to the MATLAB code) accordingly. Generated variables for the paper are included in the “data” folder in separate zip files (for liberal and conservative oxygenation strategy).
# Step 3: 
You can then transfer these files to the MATLAB data directory and run MATLAB code files. There are three code files for three experiments that we have conducted in our paper. Separate code files for synthetic, and real-world data are provided in the “code” folder.
# Step 4: 
You need to take lagged and autocorrelated links from step 1; and contemporaneous and changing modules from step 3 to get the final causal graph.
# Step 5: 
We are working to make a unified code in python that will make the whole process simple and easy to follow.
