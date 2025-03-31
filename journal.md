                                       Carbon Offset Landscapes for Data Centers
Journal

WEEK 1:

  a.	Together, we searched for more resources and found certain links of interest
  
     i.	https://www.sciencedirect.com/science/article/pii/S2214629622002468
  	
     ii.	https://www.researchgate.net/publication/224123605_Thermodynamics_of_information_technology_data_centers – Thermodynamic profiles re: data centers
  	
     iii.	https://dirt.asla.org/2024/03/01/landscape-architects-take-on-embodied-carbon/ – Current ASLA perspectives
  	
     iv.	https://gee-community-catalog.org/projects/carbon_projects/ - Carbon Offset Projects
  
      v.	https://www.unite.ai/carbon-capture-trees-ibm-nyc-machine-learning/ - Case studies re: trees, carbon sequestration tracking
    
      vi.	https://app.climatepositivedesign.com/start Current tool for carbon offset calculation given design
    
      vii.	https://onlinelibrary.wiley.com/doi/10.1155/2022/1610427#:~:text=First%2C the k-means machine learning clustering method, landscaping required by modern urban landscape design & Artificial intelligence technology based on machine learning, some simple repetitive labor at this stage
    
      viii.	Considering water and energy utilization, a study conducted at the University of Vermont using spatially-detailed records of data centers proposed strategic methods for locating data centers to minimize one or more environmental footprints. - https://vtechworks.lib.vt.edu/server/api/core/bitstreams/484c56d7-9557-4c71-ad47-84ab67a21bad/content
  
  b.	We realized that we needed need to focus on species specific with carbon offset
  
  c.	Based on these resources, Chhavi identified three datasets and tool which we plan to combine for the project
  
    i.	GLOWCAD
    
    ii.	ReforesTree
    
    iii.	I-Tree Tools
  
  d. Together, we evaluated the datasets to assess feasibility and whether they matched our overall problem.
  e. Cate conducted background research on similar projects in urban planning/ML for a basic literature review, and drafted the abstract. Chhavi edited and added necessary technical details.

WEEK 2:

- Together, we met with Nicolas on Wednesday during his OH to qualify the feasibility of our problem and assess the datasets we found. During the discussion, we came to the conclusion that we'll need to edit our focus for several reasons: a) the current way that we have posed the problem does not seem to necessitate ML (i.e. why not algorithmically select for the best tree and only use that one tree for planting?) b) with the immense carbon emissions of a single data center, any offset from landscaping would be very minimal at best c) the datasets we found may not be rigorous enough for it.
- Next, we spent some time brainstorming other ideas and challenges.
  - Chhavi explored and found other datasets related to data centers and carbon emissions.
  - Cate is qualifying them to articulate a suitable problem within our chosen field.
- As of this writing, we are trying to pivot to focus more on data center carbon emissions. Potentially: assessing the environmental impact of data center expansion or climate resilient power grid optimization through carbon-water tradeoff optimization:

    ALT IDEA 1 - REGIONAL IMPACT: Develop a model that assesses the environmental impact of adding new data centers to specific grid regions based on the existing power plant mix. Implementation Approach: Create a model that estimates both water and carbon impacts of data centers based on regional power mix. Develop a siting optimization algorithm that identifies locations minimizing environmental impact. Build forecasting models that account for projected changes in grid mix over time

    ALT IDEA 2 - CARBON-WATER TRADEOFF POWER GRID OPTIMIZATION: Implementation Approach: Apply multi-objective optimization techniques to balance carbon and water impacts. Create a recommendation system for identifying optimal generation mixes by region. (Optional: Develop interactive visualizations that demonstrate tradeoffs under different scenarios)

- Based on additional feedback from Alp, we will also strategize a way to combine the new datasets we found to see if there is a way to tackle the overall idea (natural-based systems and responses to data center emissions). So far, Chhavi had an idea to pursue carbon sequestration capacity based on drone imagery, using a dataset like Reforestree with bounding boxes and other metrics in the dataset to train regression model to identify tree type from drone image and estimate carbon capture (a limitation: not sure of more datasets present in this domain).

This coming week, we will finalize how we want to pivot our focus – making sure we have the right data – and follow up with the teaching team by mid-week to make sure that our plan is feasible before continuing.

WEEK 3:

- Chhavi explored the possible project ideas with data integration of the carbon sequestration datasets, GlowCAD and ReForestree datasets. She dropped the i-Tree dataset since it had qualitative categorical values, whereas the other two have quantitative values for the same columns. A possible idea she came across was:
  - Use reforestree imagery dataset to identify individual trees. Reforestree uses standard 50% carbon stock, instead leverage the species specific carbon stock values in GlowCAD. Three possible paths:
    - For the species available in reforestree but not GlowCAD, use ML to estimate carbon stock.
    - Use available carbon stock values to get better estimations on the ReForesTree dataset
    - Combine both
  - Potential problems:
    - Reforestree limited to Ecuador with only 28 species, as compared to GlowCAD with 864 species and global scale
    - Also reforestree dataset is highly imbalanced
    - Overlap of species might be a problem
  - Possible solution: Can look into other imagery dataset and combine them with GlowCAD instead

We both discussed and concluded that we would prefer data center problems, since these combination of datasets will lead to more time in data aggregation and EDA than ML implementation. Because of mid-terms and Cate getting sick with the flu, we were not able to work much on it though.

This week we plan to finalize the problem statement and start with dataset exploration.

WEEK 4: 

Chhavi found a new dataset that would provide ample resources for a datacenter emissions problem. Cate accordingly applied insights from past research experience and qualified a new problem and objective, which is listed below. Cate also identified some additional parameters/datasets that we may incorporate if we end up needing additional information during training.

Next week, pending feedback from Alp and the TAs, we'll get started on the code, update the abstract, and begin working on the background for the paper itself.

NEW IDEA: Optimal Site Selection for Low-Impact Data Centers

Objective: Model provides appropriate location highlighting optimal data center locations in the United States, and a method for ranking regions based on sustainability and cost-effectiveness.
1. Minimize environmental impact (low CO2, water use + availability)
2. Maximize cost-effectiveness (proximity to renewable energy, infrastructure)
3. Ensuring reliability (proximity to fiber networks and low disaster risk (this potentially would include analyzing the level of extreme weather events in a given area))

Data:
Siddik, Md Abu Bakar; Shehabi, Arman; Marston, Landon (2021). The environmental footprint of data centers in the United States. University Libraries, Virginia Tech. Dataset. https://doi.org/10.7294/14504913.v2

We've also identified some additional data sources that may supplement the analysis in the journal, but most likely will only need to use this one – the main obstacle is ensuring that the timeline and granularity of any other datasets would match. For water availability, the following is promising (https://waterdata.usgs.gov/nwis), although the data only extends to 2015. For renewable energy sources, Cate found the following –  (https://www.nrel.gov/research/data-tools, https://atlas.eia.gov/search?categories=%252Fcategories%252Frenewable%2520energy) – which could be used to further cross-reference how close the datacenters in the original dataset were to renewable energy sources.

Rationale (updated abstract to come):
As of this writing, there is no ML-based tool currently developed for optimal site selection considering environmental impact/sustainability for data centers. Similar site analysis and site selection tools are already used in real estate development (notably to identify economic patterns/trends, asset valuation, and risk management for property development).

Data Application (may need some advice on technical feasibility):
Train on existing dataset with the following variables – energy efficiency, carbon intensity with respect to water availability, infrastructure (power grid proximity and renewable energy share), spatial constraints (available land area per subbasin)
1. Geo-reference all PCA + sub basin locations
2. Feature engineering a sustainability score calculation (sum of carbon, water, renewable energy indicators), infrastructure accessibility score (distance to nearest power grid, fiber network, city)
3. Potentially also use information on proximity to fiber optic network

Remaining observations: 

(Chhavi) GIS-integration can be considered as  an extended scope based on our results from the model training. Our first goal is predicting the place based on the input, which will be listed as probable places.

(Cate) Additionally, based on my own knowledge and experience, I’d recommend some way to include weather data – specifically, avg. temperature ranges and frequency of extreme weather events. In my research, development has been driven towards areas that have 1) reliable access to infrastructure and 2) relatively stable weather to reduce disaster risk and mitigate cooling costs – hence the concentration of data centers in the mid-atlantic region, as opposed to the tornado-heavy midwest or hotter climates in southern states.


Week 6:

Cate and Chhavi made the problem statement more focused, and identified the columns to be used for the sustainability score calculation. 

Cate shared the importance of some variables like PCA generation based, and which variables can be extracted using feature engineering. She also updated the abstract.

Chhavi started work with the dataset using identified variables. She created dataframes for the calculation of carbon emissions and water intensity. 

Next week, the plan is to complete EDA, feature engineering, and start with a basic ML model training for these features.
