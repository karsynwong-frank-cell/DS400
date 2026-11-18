# DS 400 Bayesian Statistics – Final Project Proposal
 
**Name: Lehiwa Wong-Frank**
 
**Date: 11/17/26**
 
---
 
Fill this out before you start on your analysis. Write your answers under each question. A few sentences is fine for most of them. Be specific, though: "I'll look at flight loads" is too vague, but "I'll model the relationship between ticket price and available seats 2 days before departure" is better.
 
Download this file and add it to your DS400 Repository, then edit right in the github browser or in R Studio.
 
---
 
## 1. My research question
 
What do you want to find out? Phrase it as a question. Mention the place and time period if they are relevant.
 
<!-- Write your answer below this line -->
 Between 2006 and 2010, how strongly did storm-driven streamflow and suspended-sediment 
 runoff from land predict nearshore ocean turbidity in NTUs (Nephelometric Turbidity Units) 
 on the shallow reefs off the Kaulana and Hakioawa watersheds on Kahoʻolawe, and how much 
 lower was that turbidity response in the restored Kaulana watershed compared to the 
 unrestored Hakioawa watershed?
 

---
 
## 2. The dataset(s) I will use to approach my research question
 
List each dataset and where it comes from (agency, website, link). Note the format (ex .csv)
 
<!-- Write your answer below this line -->
 1. https://pubs.usgs.gov/publication/ofr20101182 (Streamflow, suspended-sediment, and 
 soil-erosion data from the Kaulana and Hakioawa watersheds, Kahoʻolawe, Hawaiʻi, 2006–2010.)
 Format: .csv / .json (directly downloadable from the USGS Water Data portal or imported into 
 RStudio via the dataRetrieval package), paired with summary tables in .pdf format from the 
 Open-File Report.
 
 2. https://pubs.usgs.gov/publication/ofr20101037 (Turbidity on the shallow reef off 
 Kaulana and Hakioawa watersheds, north coast of Kahoʻolawe, Hawaiʻi.)
 Format: .pdf (containing structured summary tables of nearshore NTU measurements, wind, 
 waves, and rainfall events off both watersheds, which I will transcribe/extract into a 
 clean .csv file for analysis in RStudio).
 
 3. https://www.kahoolawe.hawaii.gov/plans/USGS%20DOH%20II%20Turbidity%20Report.pdf
 (Turbidity on the shallow reef off Kaulana and Hakioawa watersheds, similar like link 
 number 2 just more data.)
 Format: .pdf (containing structured summary tables of nearshore NTU measurements, wind, 
 waves, and rainfall events off both watersheds, which I will transcribe/extract into a 
 clean .csv file for analysis in RStudio)
 
 4. https://www.pacioos.hawaii.edu/metadata/hi_sohdop_kaho_reserve.html (Reserve Geospatial 
 Boundaries, Pacific Islands Ocean Observing System (PacIOOS) & State of Hawaiʻi Office 
 of Planning.)
 Format: .csv / .geojson / .shp (used in RStudio with ggplot2 and sf to plot the geographic 
 locations of Kaulana and Hakioawa Gulches).
 
---
 
## 3. The specific bayesian model I will use to answer my research question
 
What methods will you actually run? For example, bayesian logistic regression, naive bayes,  etc.
 
<!-- Write your answer below this line -->
 I will fit a Bayesian Generalized Linear Model (GLM) with a Log-Normal (or Gamma)
 likelihood—specifically structured as a Bayesian Interaction Regression—in RStudio 
 using the brms (or rstanarm) package.
 
 

---
 
## 4. 3-5 peer-reviewed publications or news articles surrounding my research question
 
Give the link below. Add a sentence or two on why each source is relevant to your project.
 
1. USGS Open-File Report 2010-1182 (Peer-Reviewed Federal Report)
	Link: https://pubs.usgs.gov/publication/ofr20101182
	Relevance: This study evaluates four years (2006–2010) of streamflow and 
	suspended-sediment loads in Kaulana and Hakioawa gulches. It directly informs my research
	question by showing that restored areas in Kaulana had lower erosion and sediment discharge 
	than unrestored areas in Hakioawa.
 
2. USGS Open-File Report 2010-1037 (Peer-Reviewed Federal Report)
	Link: https://pubs.usgs.gov/publication/ofr20101037
	Relevance: This report measures shallow-reef turbidity (in NTUs) alongside rainfall and 
	stream discharge off Kaulana and Hakioawa. It provides the core empirical findings linking 
	storm runoff on land to nearshore reef cloudiness, while documenting site-specific factors 
	like wave flushing and sensor biofouling.
 
3. Estuarine, Coastal and Shelf Science – Processes Driving Reef Turbidity in Hawaiʻi 
(Peer-Reviewed Journal Article)
	Link: https://pubs.usgs.gov/publication/70033530
	Relevance: Authored by the same USGS research team (Storlazzi & Jaffe), this peer-reviewed 
	study models how waves, winds, and runoff drive turbidity variability over fringing Hawaiian 
	coral reefs. It provides physical oceanographic context and realistic parameter ranges to 
	help justify my weakly informative priors.
 
4. Frontiers in Marine Science – Large-Scale Effects of Turbidity on Hawaiian Coral Reefs 
(Peer-Reviewed Journal Article)
	Link: https://www.frontiersin.org/journals/marine-science/articles/10.3389/fmars.2022.969472/full
	Relevance: This peer-reviewed article examines how land-based sediment runoff and fine 
	particulate turbidity impact Hawaiian coral reef ecosystems. It reinforces why quantifying 
	whether watershed restoration reduces NTU spikes is critical for DLNR marine resource management.
 
5. Honolulu Civil Beat – Kahoʻolawe Holds Lessons For Maui's Environmental Recovery (News Article)
	Link: https://www.civilbeat.org/2023/12/kahoolawe-holds-lessons-for-mauis-environmental-recovery-from-the-wildfires/
	Relevance: This local investigative article highlights how KIRC's native revegetation efforts 
	on Kahoʻolawe have visibly slowed red-dirt runoff "bleeding" into the ocean. It connects my 
	historical 2006–2010 statistical analysis to modern-day watershed management across Hawaiʻi.
 
---
