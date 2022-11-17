# Material Selection Chart Method

This Python Notebook code is a tool to select material from a database using the [chart](https://www.youtube.com/watch?v=9RQkvcsRzbo&ab_channel=BillyWu) and [material index](http://mech.vub.ac.be/teaching/info/Ontwerpmethodologie/Appendix%20les%203%20Materiaal%20Indices.pdf) method

## 🔰 How does it work?
- A material database is uploaded. In this case the database was created by my students from my Selection Material Course using online free database as [Matweb](https://www.matweb.com/) and [Azom](https://www.azom.com/)
- Material database has the below information:
	- Material's name
	- Family (Ceramics, Metals, Polymers, Hybrids)
  - Price (USD/kg)
  - Density (kg/m^3)
  - Young's Modulus (GPa)
  - Yield Strength (MPa)
  - Ultimate Strength (MPa)
  - Elongation (%)
  - Hardness (HV)
  - Fracture Toughness [MPa m^1/2]
  - Melting Point
  - Source (Matweb, Azom, etc)
  - Person (who include the material information into the database)
  
 <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/1.png" width="700" >
  
 - Source and Person columns are deleted from the database
 - A bar plot (Family) and histograms for the material's properties are showed 
 
 <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/2.png" width="600" >
 
 - User has to choose two properties to create the material index. This is an example choosing Young's Modulus and Density
 
 <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/3.png" width="500" >
 
 - User must enter the exponents for each property. Based on this, the material index is created. In this example 0.5 and -1 are the exponents for Young's Modulus and Density, respectively. With these values, the material index is:
 $$\frac{E^{0.5}}{\rho}$$
 - Selection Orientation is defined for the filtering process, based on the properties' exponents. 
  - A maximization would be performed if the exponent is positive
  - A minimization would be performed if the exponent is negative
 - Material Index is calculated for each materila into the database
 - Used must set the number of material to filtering 
 - The list of materials sort by mateial index is showed
 
 <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/4.png" width = "700">
 
 - A material chart is showed
  - First property as Y-Axis and second property as X-axis
  - Each point represents a material and its color depends of the family
  - A black line represents the filter based on the number of material that user wants to classify
  - The green area is the selection region
  - The gray area is the discard region
  
  <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/5.png" width = "700">
  
 - It is possible to show a chart with the cluster families 
 
 <img src = "https://github.com/alejo1630/chart_material_selection/blob/main/images_readme/6.png" width = "700">
  
## 🔶 What is next?
- Increase the database with more materials and properties
- Create interactive charts 
- Create an interface or app
