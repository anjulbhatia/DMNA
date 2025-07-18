# Delhi Metro Network Analysis

### **Objective of the Project**
The objective of this project is to analyze the Delhi Metro network using transit data provided by DMRC (Delhi Metro Rail Corporation). The analysis will involve understanding the structure and efficiency of the network, identifying key stations and routes, visualizing the geographic distribution of stations and routes, and creating a tool to find optimal routes based on different criteria (e.g., shortest distance, minimum transfers).

This project will explore various aspects of transit network analysis, such as geospatial mapping, shortest path algorithms, station clustering, and service reliability. Additionally, an API will be developed to allow users to query routes, and a dashboard will be created for interactive data exploration.

---

### **What You Will Find in This Notebook**
In this notebook, we will:
1. **Load the Data** from the DMRC_GTFS source directory.
2. **Clean and Preprocess** the data for further analysis.
3. Perform **Exploratory Data Analysis (EDA)** to identify patterns and insights in the metro system.
4. Implement **Network Analysis** to understand connectivity and optimize routes.
5. **Visualize the Metro Network** using geospatial maps.
6. Build an **API** for querying routes and a **Dashboard** to explore and visualize data interactively.

---

### **About The Dataset**
The dataset used for this project is available at [Open Transit Data](https://otd.delhi.gov.in), published by the Department of Transport (Govt of NCT of Delhi) in collaboration with IIIT-Delhi. The dataset includes both static and real-time transit data, encouraging the development of innovative and inclusive transportation solutions. This project utilizes the **static** dataset provided for the **Delhi Metro**.

The static data is packaged in **DMRC_GTFS.zip**, which contains the following files:

| **File Name**     | **Description**                                                                 |
|-------------------|---------------------------------------------------------------------------------|
| `agency.txt`      | Details of transit agencies providing services in the dataset.                  |
| `calendar.txt`    | Weekly schedule with start and end dates for transit services.                  |
| `routes.txt`      | Transit routes, each representing a group of trips displayed to passengers.      |
| `shapes.txt`      | Defines the path followed by vehicles (route alignments).                       |
| `stops.txt`       | Information on stops, including station names, descriptions, and geospatial coordinates. |
| `stop_times.txt`  | Arrival and departure times for each trip at the respective stops.              |
| `trips.txt`       | Trips for each route, including sequences of stops during specific time periods. |

Source: [Open Transit Data Delhi](https://otd.delhi.gov.in/data/staticDMRC/)  
Last Updated: August 10, 2023

---

### **Key Questions Addressed by the Project**
1. **What is the structure of the Delhi Metro Network?**  
   We will map out the entire network, visualizing the routes and stops to understand the geographic coverage of the system.

2. **Which stations and routes are the most critical?**  
   Using network analysis techniques, we will identify key stations (e.g., those with the most connections or highest service frequency) and routes (e.g., the most frequently traveled or strategically important).

3. **How can we optimize travel within the metro system?**  
   We will use graph algorithms to find the shortest routes between two stations and minimize transfers, considering both distance and travel time.

4. **What insights can we gather from the transit data?**  
   Exploratory Data Analysis (EDA) will help uncover patterns in station usage, route efficiency, service reliability, and more.

5. **How can users query and interact with the data?**  
   We will build an API and a dashboard to allow users to explore routes, find optimal travel paths, and visualize network insights in an interactive way.

---

### **Project Workflow**
1. **Data Cleaning and Preprocessing:**  
   Load the raw data from `DMRC_GTFS.zip`, clean and preprocess it for analysis (removing null values, handling missing data, and converting date and time formats as needed).

2. **Exploratory Data Analysis (EDA):**  
   Visualize the distribution of stations, routes, and services. Analyze key metrics like station distance from the first station, the frequency of trips, and peak hours of operation.

3. **Geospatial Mapping and Visualization:**  
   Use the `shapes.txt` and `stops.txt` files to plot the metro network on a map, visualizing routes and station locations using mapping libraries like `folium` or `geopandas`.

4. **Network Analysis:**  
   Treat the metro system as a graph, where stations are nodes and routes are edges. Perform:
   - Shortest path analysis.
   - Station importance (e.g., degree centrality).
   - Route optimization with minimal transfers.

5. **API and Dashboard Development:**  
   - Build a **FastAPI** service that allows querying routes and retrieving shortest paths and travel times.
   - Create an interactive dashboard using **Streamlit** or **Dash** to visualize the metro network, show station data, and provide route recommendations.

---

By the end of this project, we aim to provide both a **deep dive into the structure of the Delhi Metro** and **tools for real-time analysis and route optimization** that can be extended for public use.
#   D M N A  
 