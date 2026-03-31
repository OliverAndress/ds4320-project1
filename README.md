# DS 4320 Project 1: Predicting Carbon Offset Success Using Relational Risk Modeling

## Executive Summary
[To be completed]

**Author:** [Oliver Andress]  
**NetID:** [csg7su]  
**DOI:** [To be created]  
**License:** [MIT License](LICENSE)

### Quick Links
- **Press Release:** [Press Release] <INSERT LATER> 
- **Data:** [OneDrive Data Folder](<https://myuva-my.sharepoint.com/:f:/r/personal/csg7su_virginia_edu/Documents/DS4320-Project1-Data?csf=1&web=1&e=9I78y4>)
- **Pipeline:** [Analysis Pipeline](<INSERT LATER>)

---

## Problem Definition




**General Problem:**


Forecasting Global Climate Change(General Problem #4, DS 4320 Project 1 Rubric)


**Refined Specific Problem:**


The primary challenge in carbon market analysis is the "Selection Bias" inherent in registry data, as the dataset only includes projects that successfully cleared the rigorous initial registration process. Consequently, this project defines success not as **Market Utilization**.


The specific problem is to predict whether a registered reforestation initiative will be **Effective** (demonstrating high credit retirement rates and consistent issuance) or **Underperforming** (functioning as a "Ghost Project" with issued credits that fail to reach the market). By leveraging registry affiliation, geographic region, and project type, the model identifies the risk factors that lead a registered project to stall or fail in its operational phase.


**Rationale:**


Forecasting Global Climate Change is a massive, multifaceted domain. Investigating this at a global scale would require multi-decade time-series data. I do not have the current capabilities to structure that into a traditional relational model within the scope of this project. By narrowing the scope to the **Voluntary Carbon Market**, the broader issue is transformed into a manageable classification problem. This allows for a deeper exploration of the integrity and effectiveness of specific climate interventions (reforestation) using a 3rd Normal Form relational structure. 

**Motivation Paragraph**


I took a half-semester class this semester on Climate Investing. I learned a lot but the two things that particularly stood out was the impending danger of climate change in all walks of life and the ability for young people to have the ability to make the world a better place while also making money. We also talked a lot about the benefits of Carbon Credits, where corporations or organizations buy carbon credits to offset their emissions. However, many projects fail to protect forests, leading to a term called Greenwashing (where companies outwardly appear to be environmentally friendly when they are not). I want to use what I have learned in my class and through my Data Science Major to try to predict a project's success before capital is committed. This ensures that money is efficiently allocated to the initiatives that will help make the world cleaner, therefore helping reduce the impact of climate change. While initially this was going to be a prediction of whether or not a specific carbon market initiative would be approved, I wanted something that was more morally grey. There will be some companies that appear on the Berkeley data set that appear good from the outside, but after analyzing, will soon be mischievous. 




