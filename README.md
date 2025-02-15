# GPS Trip Analysis and Map Matching
Overview

This project analyzes GPS trip data, detects stop zones, and visualizes routes using Folium. It also integrates map-matching techniques with PyTrack to align raw GPS data to road networks.

Features:

  GPS Data Processing: Reads and processes trip data from a CSV file.
  
  Stop Zone Detection: Identifies stop zones based on time and distance thresholds.
  
  Interactive Map Visualization: Uses Folium to visualize trip routes and stop zones.
  
  H3 Indexing: Groups locations using the H3 geospatial indexing system.
  
  Map Matching: Matches GPS points to the road network using PyTrack.
Requirements:
  pip install numpy pandas h3 haversine swifter networkx tqdm folium pytrack
  
Map Matching Overview : 

  Map matching is essential to correct GPS positioning errors caused by satellite inaccuracies, transmission issues, and environmental factors. Raw GPS trajectories often deviate from actual road networks, affecting applications like traffic analysis, ride fare estimation, and self-driving simulations. By integrating GPS data with OpenStreetMap, map matching reconstructs accurate trajectories, ensuring reliable navigation, data cleaning, and improved visualization. 

Map Matching Workflow: 

    Extracts bounding box from trip data.
    
    Retrieves road network graph from OpenStreetMap.
    
    Identifies candidate road segments.
    
    Constructs a trellis graph for sequence alignment.
    
    Runs Viterbi algorithm for optimal path matching.
    
    Displays the matched route on the map.

Resources :

Map Matching paper : https://ieeexplore.ieee.org/document/9927417
Uber's H3 library : https://www.uber.com/en-TW/blog/h3/
