# Personalised Skincare Recommendation System 

## Executive Summary
### Business Challenge
The business challenge addressed was the lack of personalised skincare product recommendations, which often result in users buying products that do not adequately meet their needs. Many consumers face difficulties in finding suitable skincare products due to generic and one-size-fits-all recommendations. The hypothesis was that by leveraging user-specific data and clustering techniques, a recommendation engine could deliver more accurate and personalised skincare suggestions. This project, therefore, aimed to develop a personalised skincare recommendation app that caters to individual skin characteristics. At the heart of this app is a recommendation engine, designed with a structured logic workflow (see Figure 1) to provide tailored skincare suggestions.

![engine workflow](assets/img/Picture1.png)

Figure 1. Recommendation Engine Logic Workflow.

### Methods - Data Collection
The following data was used:
(1)	[Sephora product review data from Kaggle](https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews)
(2)	Synthetic user data from Mockaroo
(3)	Real-time weather data from the OpenWeatherMap API

### Methods - Data Processing
Data processing involved quality checks, cleaning, merging, and feature engineering using Python. Exploratory Data Analysis (EDA) was conducted on the Sephora and synthetic user datasets to understand the underlying patterns.

### Methods - Data Analysis
K-modes clustering was applied to the synthetic user data to group users with similar skin characteristics (e.g., skin type and skin concern). The analysis was conducted using Python.

### Results
Three clusters were identified, each with unique profiles characterised by specific skin types (e.g., dry), concerns (e.g., aging), and preferred ingredients (e.g., retinol). These profiles guided the recommendation engine in filtering products, leading to the development of an app that offers personalised skincare recommendations.

### Conclusion
The app performs well but could benefit from integrating more environmental factors and regular updates to the clustering model. Future expansions should focus on incorporating additional data, such as products from other retailers, and refining the recommendation accuracy.

##  Data Preparation
The project adhered to Extract, Transform, and Load (ETL) standards throughout the data preparation stage, ensuring a systematic and efficient process.(1) An ETL workflow was planned and developed to guide data collection, cleaning, transformation, and loading (see Figure 2).

![etl workflow](assets/img/Picture2.png)

Figure 2. Diagram of the ETL pipeline. Capabilities include analytics, insights, and visualisations.

### Data Collection

The first stage involved data collection and extraction, which included downloading the publicly available Sephora product review dataset from Kaggle and generating synthetic user data from Mockaroo. The Sephora dataset comprised five review CSV files and one product information CSV file. This data was processed first to inform the unique values needed for the synthetic user data columns. Once the Sephora data was processed, synthetic user data was generated using Mockaroo, a versatile online tool for creating realistic fake datasets.(2) Six fields were defined to create the desired dataset (see Figure 3). The "primary_skin_concern" column was weighted using skin concerns data from Statista(9) to reflect real-world nuances accurately.

![Screenshot of Mockaroo Generator](assets/img/Picture3.png)

Figure 3. Screenshot of data fields created in Mockaroo for the synthetic data.

### Data Transformation

## References
1. [The Power of ETL Piplines Tools and Best Practices](https://medium.com/@xhackfuel/the-power-of-etl-pipelines-tools-and-best-practices-e419688882b8)
2. [Mockaroo to the Rescue](https://plgah.medium.com/need-synthetic-data-mockaroo-to-the-rescue-e9c8159b0d9f)
