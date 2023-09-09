# Remote Early Detection and Biosecurity Response 

A Reporting Tool for Livestock Owners 

## Solution Overview 

The project will develop existing technology currently used for plant disease and pest detection and biosecurity reporting in the Northern Australian pastoral sector to assist with the emerging threat of a number of significant emergency animal diseases at the northern Australian border, including Foot-and-Mouth (FMD) and Lumpy Skin Disease (LSD) in Indonesia and African Swine Fever (ASF) in Indonesia, Timor Leste and Papua New Guinea. Industry and Government will partner together to ensure early detection and rapid response is achieved when these diseases enter Australia and that small targeted investments are made now in innovative tools to overcome the exceptionally limited resources we have in the north to cover such a large geographical area. 

![Early Warning System](Early%20Warning%20System%20v2.png)

## Solution Approach 
The approach for this solution is to create a Proof-of-concept (PoC) system for early detection and rapid response of emergency animal diseases (EADs). This will consist of: 
* A web form for the pastoral sector to report suspect diseases including photos, location and contact information 
* An AI engine to screen the photos against a library and triage them with a probability estimate. This will be built for FMD (Foot and Mouth Disease) and LSD (Lumpy Skin Disease). 
* A spatial database that matches reports against properties (PICs from NLIS) 
* A workflow to pass reports to the responsible agency for action in a format where they can be ingested to MAX 
* A reporting system to enable central monitoring of reports and workflow progress.

## The Threat

Emergency animal diseases (EADs), including lumpy skin disease and foot and mouth disease, are not known to be present in Australia and it is considered to be in the national interest for the country to be free (exotic disease). They have the potential to cause devastating impacts to the livestock industries of Australia with serious economic and social implications along with affecting animal, human, and environmental health. An outbreak of an EAD could result not only in animal deaths and production losses, but trade restrictions would cause severe economic impact. 

Meat and wool production by the cattle and sheep industry contributed almost 30% to the gross value of agricultural production in Australia, providing employment opportunities and supporting rural communities. The beef industry is the largest agricultural enterprise in Australia, which is a world leader in the export of beef and live animals. The number of cattle varies from year to year between about 25 and 30 million, and most of the exports are in the form of processed beef, which is sent mainly to Japan, the United States, and South Korea. 

According to a 2022 update of ABARES 2013 estimate, a large multi-state FMD outbreak would have an estimated direct economic impact over 10 years of around $80 billion (in $2020-21 dollars). The primary impact of an FMD outbreak would be to trade and the economy. As soon as FMD was detected, Australia would lose most of its meat export markets, especially the premium ones. FMD can cause significant production losses in a livestock industry, leading to a decrease in the supply of animal products such as meat, milk, and eggs. The social impacts of the disease would also be significant, including job losses and reduced income for farmers and rural communities. If the disease arrives, the control method is to lock down the movement of animals around Australia and to control the disease through culling. This is conducted in concentric circles around infected properties. This creates a firebreak, and most animals culled will be preemptively killed to stop the spread. Lockdowns would also hamstring another major Australian industry: already reeling from the effects of Covid, tourism.

It is important to note that Australia has been free of FMD since 1872 due to stringent pre- and post-border measures. However, many of Australia's neighbors in Asia are not as fortunate, with endemic FMD at a resultant high socio-economic impact. Therefore, it is crucial to have measures in place to prevent, detect, and respond to FMD in Australia. Australia has a detailed plan called AUSVETPLAN, for responding to emergency disease outbreaks, and the Australian EAD Response Agreement (EADRA) that establishes responsibilities of governments and industry. An important strategy is early reporting of EADs, and there has long been in place the Emergency Animal Disease Watch Hotline for reporting by phone. This project is designed to enhance early reporting, using modern technologies of smartphones, AI, the web, the cloud and spatial data systems.

## Contingencies
The project is less a development of existing approaches, than a new approach using modern, robust technologies with considerable complexity. The very short time frame dictates we can provide a PoC with only limited testing and integration with agency systems. These aspects will need to be followed up outside this PoC project. While the PoC is technically highly achievable, the short time frame creates a signficant risk of milestone over-run. A risk management framework will be used through the system build and testing that captures and assesses risk via a Risk Management Framework. 

## Solution Architecture AI

Leveraging the experience in plant disease and pest detection as well as the Healthy Country AI Project is a Custom Vision AI service that provides the platform to label data and transfer human intelligence to machines.  The taxomonies for these Custom Vision AI models include two sets of models for labelling :
* Model 1 - Species (Cow, Horse, Pig etc)
* Model 2 - Disease (Foot and Mouth, Lumpy Skin, etc)  

Initial models will focus solely on species of Cattle only and for priority diseases being FMD and LSD.

![Early Warning System AI](Early%20Warning%20System%20AI.png)

## Project Activity

![Project Activity](Project%20Activity.png)

## Project Scope 
 
* COMPONENT 1 - Build a web form for producer to submit a geotagged report with photos, user details, etc.  
• Test web form with producers 
Cooperate with trials organised by the project lead 

* COMPONENT 2 - Reports are ingested to a Konect database with spatial capability  
Konect account to be held by AgKonect 
• Database has API link to NLIS to link report to PIC 
Access to NLIS API to be provided
 
* COMPONENT 3 - Build AI system for triaging LSD and FMD  
• Needs a dataset – lots of photos that can be labelled as +ve or -ve 
 To be provided and labelled 
• Train the system on the dataset
• Use Testing data that is different to the training data
• Form workflow triggers AI assessment of the photo with a probability estimate returned to a handler 
• Form is forwarded to actioning agency (state biosecurity dept.) in format to be ingestable to MAX.  MAX format to be provided 

* COMPONENT 4 - Database is reported on web, e.g. embedded Power BI 
PoC will be housed by AgKonect Power BI Embedded portal 
• System is housed at a suitable location for interaction with all stakeholders 
• Business rules are developed, e.g. responsibilities, privacy of data, access rights and system 
• Agency actions with appropriate investigation and communication with submitter 
• Agency reports back to system to close the loop, record is updated
• We don’t know the best approach to this until agencies have been engaged 
• System checks with submitter if they have been advised by agency
• We will provide an automated email receipt to report submitters, asking them to call the EAD hotline if they do not receive a response to their report in a satisfactory time 
 
