# Analyzing Ride Patterns and Predicting Demand to Optimize Ride-sharing Services

- For uploading the large files use lfs in git
- install using : git install lfs
  
Follow the steps : 
- Create a virtual environment :
  * python -m venv venv         --> step to create venv
  * .\venv\Scripts\Activate     --> Activate env
  * Add the packages You need to install inside the requirements.txt file.
  * Set the Python Interpreter.

- Notebook : 
  1. Ride Demand Prediction : 
  Note : If dataset not available download from "https://www.kaggle.com/datasets/fivethirtyeight/uber-pickups-in-new-york-city/data" ~~here
  * We have 4 group of datasets: 
    a) Uber trip data from 2014 (April - September), separated by month, with detailed location information
    b) Uber trip data from 2015 (January - June), with less fine-grained location information
    c) non-Uber FHV (For-Hire Vehicle) trips. The trip information varies by company, but can include day of trip, time of trip, pickup location, driver's for-hire license number, and vehicle's for-hire license number.
    d) aggregate ride and vehicle statistics for all FHV companies (and, occasionally, for taxi companies)

  Q.) Why c) & d) are excluded from prediction dataset?
  * From these c) --> Inconsistent location info
                  --> Inconsistency in column format
                  --> Most FHV files lack precise lat/lon or even zone IDs.
               d) --> No date/time or spatial data.
  * IMP Hence, c) & d) datasets ignored them for accurate predictions. 

  Q.) Why considered only 2014 Data finally to process, predict_demand & use for visualization?
  * 2014 data gives exact lat/lon coordinates, 2015 data that only has zone IDs.
  *  Final Summary You Can Say in Interview:
      “I chose to work with the 2014 dataset alone as it provided detailed location data, which was essential for building a spatial-temporal model. This allowed me to focus on capturing real-world demand patterns accurately, without worrying about inconsistencies or merging complexities.”

  Q.) 
      