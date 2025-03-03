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

- Based on additional feedback from Alp, we will also strategize a way to combine the new datasets we found to see if there is a way to tackle the overall idea (natural-based systems and responses to data center emissions). So far, Chhavi had an idea to pursue carbon sequestration capacity based on drone imagery, using a dataset like Reforestree with bounding boxes and other metrics in the dataset to train regression model to tdentify tree type from drone image and estimate carbon capture (a limitation: not sure of more datasets present in this domain).

This coming week, we will finalize how we want to pivot our focus – making sure we have the right data – and follow up with the teaching team by mid-week to make sure that our plan is feasible before continuing.
