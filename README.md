# Bing News Analytics 🌐

Welcome to the Bing News Analytics project! This Data Engineering project leverages Microsoft Fabric to transform raw news data from the Bing API into insightful reports with end-to-end data processing and analysis.

## About the Project

This project involves ingesting news data daily from the Bing API and generating insightful reports through a comprehensive data pipeline. The project covers data ingestion, transformation, sentiment analysis, orchestration, reporting, alert configuration, and thorough testing to ensure data integrity and reliability.

## Topics Covered

1. **Data Ingestion from Bing API using Data Factory:** 
   - Pulled in data from Bing using the Bing API, utilizing the news endpoint and applying headers with query parameters to filter the data to the last 24 hours. Dynamic content was used to generate content based on a given category. The API key was generated in Azure, and the data was saved into a JSON file.

2. **Data Transformation using Synapse Data Engineering:** 
   - Shaped and refined raw JSON data into a curated Delta Table, including techniques like incremental loading to maintain efficiency. The transformation process included filtering rows by removing null values and unimportant columns like images, and formatting the date and time published column to only include the date. All the code used in the notebook was written in PySpark.

3. **Sentiment Analysis using Synapse Data Science:** 
   - Predicted the sentiment of the news, classifying it as Positive, Negative, Mixed, or Neutral by analyzing the news descriptions. This was done using Synapse Data Science, importing the model from the Synapse ML services library, and creating a separate column for the sentiment predicted for each news description in the table.

4. **Orchestration using Data Factory via pipelines:** 
   - Ensured smooth and efficient operations by orchestrating data workflows.

5. **Data Reporting using Power BI:** 
   - Visualized data in a compelling and actionable manner, creating measures for the sentiment in Power BI and exploring the Auto-generate feature.

6. **Configuring Alerts using the Data Activator:** 
   - Set up alerts and notifications within Power BI visuals using a new tool called Data Activator to stay ahead of potential issues. The alerts were tested, and notifications were received via Microsoft Teams.

7. **End to End Pipeline Testing:** 
   - Validated the integrity and performance of pipelines, ensuring reliability and accuracy from data ingestion to report updates.

## Getting Started

### Prerequisites

- Microsoft Azure Subscription
- Create a new data resource for the project and then add Bing API and Microsoft Fabric.

### Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/SSunilDV/Bing-News-Analysis.git
   ```
2. Set up Data Factory in Microsoft Fabric for data ingestion.
3. Create a data lake house in Synapse Data Engineering.
4. Configure Synapse Data Engineering for data transformation (which includes the data pipeline).
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

- **LinkedIn:** [Sunil Durga Venkat](https://www.linkedin.com/in/sunil-durga-venkat/)
- **Email:** [Gmail](mailto:sdvsurimalla@gmail.com), [Outlook](mailto:sxs6577@mavs.uta.edu)

Project Link: [Bing-News-Analytics](https://github.com/SSunilDV/Bing-News-Analysis)

## Acknowledgements

- [Microsoft Azure Documentation](https://docs.microsoft.com/azure/)
- [Synapse Analytics](https://docs.microsoft.com/azure/synapse-analytics/)
- [Power BI](https://docs.microsoft.com/power-bi/)
- [Data Factory](https://docs.microsoft.com/azure/data-factory/)
