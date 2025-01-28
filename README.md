# kessler-exploration
This repository focuses on obtaining and parsing satellite two-line-element (TLE) data, and assessing the density of objects in low-Earth orbit (LEO). 

The process is currently split into two Jupyter notebooks:
  1. TLE Queries
       - Queries Space-Track.org to pull TLE data by month to create an SQL database of satellites and their TLE history.
  2. TLE Parsing
       - Reads in TLE data to extract satellite information (x,y,z positions, velocity vector, launch date)
       - Uses Simplified General Perturbation 4 (SGP4) to propogate satellites orbits by using positions and velocity vector
       - Calculates pairwise distances between satellites (currently only done for this month's TLE data)
    
To do list:
  - Read in TLE history and assess pairwise distances as a function of time
  - Simulate positions and tracks for predicted numbers of mega-constellations set to go active by 2030, and recalculate pairwise distances
  - Extrapolate trend of LEO satellite launches to 2050 and repeat pairwise distance calculations
  - Simulate orbital collision in a mega-constellation orbital shield and assess pairwise distances
  - Explainer for process
