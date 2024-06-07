# Bing News Analytics 🌐

Welcome to the Bing News Analytics project! This Data Engineering project leverages Microsoft Fabric to transform raw news data from the Bing API into insightful reports with end-to-end data processing and analysis.

## About the Project

This project involves ingesting news data daily from the Bing API and generating insightful reports through a comprehensive data pipeline. The project covers data ingestion, transformation, sentiment analysis, orchestration, reporting, alert configuration, and thorough testing to ensure data integrity and reliability.

## Topics Covered

1. **Data Ingestion from Bing API using Data Factory:** 
   - Pulled in data from Bing using Bing api while using the news endpoint and also using the headers with query parameters inorder to filter to last 24hours, setting the foundation for the analytics project. Also used the dynamic content in order to generate content based on given category. The key for the api is generated in Azure. In the end the data is saved into a JSON file.
   
2. **Data Transformation using Synapse Data Engineering:** 
   - Shaped and refined raw JSON data to a curated Delta Table, including techniques like incremental loading to keep processes efficient. This Data Transformation includes the filtering of rows by removing null values and removing unimportant columns like images and further formating the date and time published column to only date. All the code used in the notebook was PySpark.

3. **Sentiment Analysis using Synapse Data Science:** 
   - Predicted the sentiment of the news classified as Positive, Negative, mixed or Neutral by analyzing the news description. This was done using the synapse data science where importing the model from synapse ml services library and then making a seperate column for the sentiment predicted for each news description in the table.

4. **Orchestration using Data Factory via pipelines:** 
   - Ensured smooth and efficient operations by orchestrating data workflows.

5. **Data Reporting using Power BI:** 
   - Visualized data in a compelling and actionable manner also by creating the measures seperately for the sentiment in Power BI and also explored the Auto generate feature.

6. **Configuring Alerts using the Data Activator:** 
   - Setting up alerts and notifications within Power BI visuals using a new tool called Data Activator to stay ahead of potential issues. The Alerts were tested where the alert was received using Microsoft teams.

7. **End to End Pipeline Testing:** 
   - Validated the integrity and performance of pipelines, ensuring reliability and accuracy from data ingestion to report updates.


## Getting Started

### Prerequisites

- Microsoft Azure Subscription
- Create a new data resource for the project and then add Bing Api and Microsft fabric.

### Installation

1. Clone the repository
   ```sh
   git clone https://github.com/SSunilDV/Bing-News-Analysis.git
   ```
2. Set up Data Factory in Microsoft Fabric for data ingestion.
3. Create data lake house in the synapse data engineering.
4. Configure Synapse Data Engineering for data transformation(which includes the data pipeline).
5. Implement sentiment analysis using Synapse Data Science.
6. Set up Data Factory pipelines for orchestration.
7. Create Power BI reports for data visualization.
8. Configure alerts using Data Activator.
9. Test the entire pipeline for reliability and accuracy.

### Usage

1. Run the Data Factory pipeline to ingest data from the Bing API.
2. Transform the raw data using Synapse Data Engineering.
3. Perform sentiment analysis on the transformed data.
4. Visualize the results in Power BI.
5. Monitor and receive alerts for data anomalies using Data Activator.
6. Regularly test the pipeline to ensure seamless operation.


## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

LinkedIn - [Sunil Durga Venkat](https://www.linkedin.com/in/sunil-durga-venkat/)

Mail - [Gmail](sdvsurimalla@gmail.com) , [Outlook](sxs6577@mavs.uta.edu)

Project Link: [Bing-News-Analytics](https://github.com/SSunilDV/Bing-News-Analysis)

## Acknowledgements

- [Microsoft Azure Documentation](https://docs.microsoft.com/azure/)
- [Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/)
- [Power BI](https://docs.microsoft.com/power-bi/)
- [Data Factory](https://docs.microsoft.com/azure/data-factory/)
