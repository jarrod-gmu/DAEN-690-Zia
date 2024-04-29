# DAEN-690-Zia
TEAM MEMBERS
Jarrod Clark
Ryan Wadsworth
Sudha Jain
Sean Coombs
Jason Myslewski

INSTRUCTOR 
Dr. Brett Berlin

PROBLEM DESCRIPTION
Since 2015, the United Nations rallies governments, private sector and civil society around 17 Sustainable Development Goals (SDGs) for a better future, in a roadmap to alleviate health, social, political and economic problems.
In a call for partnerships between stake holders of all levels, Goal 17, “Partnerships For The Goals” encourages to “Strengthen the means of implementation and revitalize the Global Partnership for Sustainable Development” 
(Goal 17 | Department of Economic and Social Affairs, n.d.), through higher inclusion of the least developed countries in the trade system as well as resources, expertise and technology sharing to build their self-sufficiency.
The SDGs progress is monitored by series of indicators.  It is a complex and multidimensional dataset that has reached 2.7 millions records in 2023, provided in CSV and/or JSON formats. There is a need for a more effective 
visualization approach (than traditional 2D graphs), as to enable a holistic vantage point that allows project participants to better understand the complex relations surrounding the goals.

PROJECT GOALS
We aim to enhance the presentation of the SDGs to aid decision-making at the higher-level and facilitate actionability at the grass-root level through improved communication of key insights within these inherently complex systems.  
Enabling stakeholders to see how their piece of the puzzle relates to other key players, so that they may better know who to communicate with and how to communicate actionable information.

Deliverables include a 3D interactive visualization of the partnerships surrounding all 17 of the Sustainable Development Goals using the GaiaViz system.
NOTE: The minimum system requirements to run the GaiaViz software is a computer system with an Intel I7 or higher processor, 8 GB RAM, 1TB disk storage, and a dedicated GPU.

HOW TO CREATE THE VISUALIZATION:

The main function, that creates the visualization, is broken into 3 parts; data conditioning, geocoding, and visualization creation. 

The first step is data conditioning which is performed by the UN SDG Data Conditioning.ipynb Jupyter notebook. To use this tool you must download the UN SDG dataset from https://unstats.un.org/sdgs/indicators/database/archive, currently 
the code uses the 15-Dec-23 release named "2023_Q3.2_AllData_Before_20231215.csv". It is untested but theoretically conditioning should work for any release 15-Dec-23 or later. This file is received as a zip and should be extracted into 
the same folder containing the code. The kernel needs to have pandas, re, json, seaborn and matplotlib.pyplot libraries installed to run this notebook. The resulting file "2d SDG dataset.csv" will be created in the working directory.

The second step is geocoding, performed by the Geocoding.ipynb Jupyter notebook. This step requires the "2d SDG dataset.csv" file output of the data conditioning step. It also requires pandas, pycountry, and geopy libraries installed on
the kernel. Once the necessary libraries are installed just run all cells. The output of this is a file called "GeoLocationInfo.csv" which is created in the working directory.

Last for creation of the visualization. Make sure the "colors.csv", "np_node-template.csv" and "np_tag-template.csv" files are in your working directory and open the drop_pins.ipynb Jupyter notebook. This notebook requires pandas, os, 
rapidjson and numpy libraries.The code can be run all at once, taking about 4 minutes from start to finish. Currently the data output is written to specific node and tag files in a GaiaViz Prototype file, but this isn't necessarily the 
only way to implement. Your choice of how to save the csv will depend on how you plan to use the resulting files. As it stands now, the resulting files need to be opened in Microsoft Excel spreadsheets and resaved, unchanged, in order to 
address an unresolved datatype mapping issue. 

To view the resulting visualization, open the GaiaViz application and load the batch file for the prototype to which the node and tag files were written.

EXTRA FILES FOR DATA EXPLORATION:

1. UNSDGCleanGeoArea.ipynb - Notebook to produce a list of countries with corresponding ISO geoarea codes.
2. UNSDGDataStructure - A useful notebook to be used to verify the contents of the raw data file are uncorrupted.
3. DAEN_690_Project_Revised.ipynb - Notebook containing the code for summarizing series descriptions.
4. ExploratoryDataAnalysis.ipynb - Notebook containing code for Initial Data Exploration
