![My Image](https://github.com/Wishwa-code/Ceylon2World/blob/main/c2w-logo.png)

<div align="center">
  <h1> Ceylon2World</h1>
  <h2> (C2W): Empowering Agri-SME owners to discover lucrative export markets and navigate the exportation journey</h2>
</div>

# Abstract

Sri Lanka is a developing nation, heavily relies on its Small and Medium Enterprise
(SME) sector, which accounts for 75% of the total enterprises in Sri Lanka. Agri-SMEs,
comprising over 75% of all SMEs in Sri Lanka, play a crucial role in the national
economy. However, despite the Sri Lankan policy standards framework developed to
foster the SME sector development, majority of the SME ventures that start within Sri
Lanka are closed down after three years of commencement and 60% of them occur
within the first two years. Given the circumstances of the situation, it is clear that
necessity for a solution to address this issue.

Through a comprehensive literature review, key challenges faced by SMEs during
internationalization were identified. These challenges encompass lack of capital,
insufficient infrastructure, lack of innovation and market information, higher
competition, obsolete technology and managerial skills. Exporters’ and domain
expert’s questionnaire were further employed to validate these findings and gather
insights. Apart from the initial challenges users mentioned challenges such as finding
new markets and new market opportunities were identified. Also, users mentioned that
export becomes riskier due to lack of structured system to facilitate transactions with
buyers and information to identify safe shipping routes including risks and
opportunities involved. Based on above data system requirement application was
created to build a business intelligence application to provide exporters with required
information to make effective decisions while facilitating an environment to build
healthy relationships with other buyers and exporters.

The incremental and iterative approach was employed to build the final prototype of
“C2W”. Final solution consists of all the core functionalities and the basic structure to
implement the escrow system. Furthermore, underlying infrastructure is developed to
scale the final solution to serve the target audience with growing data needs.

Finally, solution was evaluated by subject matter experts and technical expert based on
concept and design to ensure the reliability, accessibility and the security of the final
solution.

> [!NOTE]
> This is my final year project and initially I wanted to select a problem that is actually faced by the community rather than finding a solution for a problem in a domain that is already populated with many technological solutions. I found article for sri lankan statistics department(incuded in my report) that proves 70% Sri Lankan Agri SMEs are getting closes before they complete
> three years from the start. After reseaching problem background and successfully completing pilot study which included 10 representatives from different categories of SMEs, it was evident that main sri lankan Agri SMEs having issues is sri lanka's highly saturated markte which is dominated by
> multi-national corporations. 4 out of 6 issues that was mentioned by all representatives and proved by data, were succesfully addressed by proposed solution regardless of the government and politics related limitations. Following the foundations of initial goals outlined in the requirement elicitation phase,
> main goal was to build a application that could predict the demand for the sri lankan products in foreign markets for the upcoming months. Data was collected from [UNComtrade website](https://comtradeplus.un.org/), according to initial requirement python language and flask framework selected to automatically create
> xgboost models for each product and each country (combintion of each country and product will have one trained model), staff users will be able to update data for each product and models will be automatically trained with new data. React was selected create frontend application. Following requirements were added as should have requirements.
>
- [x] Let user select product and country to view demand for 5 upcoming months
- [x] Let user view news feed which displays news update catered to user profile
- [x] Let user view trending products in different market place around the world to identify new exorting products
- [x] Provide user with collection of tutorials to learn exporting
- [ ] Let users make transactions with other users (final goal is to create a escrow system where both buyer and exporter users are bound to complete transactions)
- [x] Let users manage their profile where they can view bookmarked news articles, products, other connected users as buyers or exporters.

- Automated prodedure was implemented to create and store everytime new datasets of export data of a product in a certain country. When updates for the each dataset is made, new model will be trained and stored to make calculations for that product. Eventhough training seperate
xg boost models for each dataset can generate more accurate results, generating predictions every time when user make request is highly resource intesive. Given that this is research project, main focus was to create more accurate models for each combination of 10 products in 11 countries(listed in the report), which is 111 datasets even for such
a small sample. Only data for 24 months was available for all the datasets and models was able to achieve avarage 67% accuacy. 

- Frontend application was directly connected to bloomberg API to get news updates and when users bookmark they were separately stored in mongodb.

- Collection of products fetched from ebay, temu, alibaba public APIs was filtered and delivered to users on request based on country and product.

- Collection of  domestic business interested in given product fetched from google business api was delivered to user on request based on country and product.

- Only part of frontend page for escrow fucntionality was built given that building escrow system takes considerable time given limited time scope.

> [!TIP]
> Please refer to the final project report documentation in this repo for more details. :shipit:

## Setup

-> populate mongodb with data from csv files in backend.

-> run the flask app in backend directory and connect with mongo db.
-> run the frontend react application in frontend directory.

-> now once you select the product and country it will take some time to generate models on the fly you can see output of the models from flask terminal.

-> thank you~🐳
