### Prerequisites
- Docker and Docker Compose installed (for easy setup of Elasticsearch and Kibana)
- Basic knowledge of Elasticsearch queries
- Familiarity with Kibana visualizations

### Setup Instructions
1. **Clone the Repository**

2. **Start Elasticsearch and Kibana**
   ```sh
   docker-compose up -d
   ```
3. **Verify Services**
   - Elasticsearch: http://localhost:9200
   - Kibana: http://localhost:5601

### Data Ingestion
- Use the provided JSON file for salaries and restaurants data.
- Import the data using:
  ```sh
  curl -X POST "http://localhost:9200/salaries/_bulk" -H "Content-Type: application/json" --data-binary @salaries.json
 



### Kibana Visualization
1. Open Kibana at http://localhost:5601
2. Create an index pattern for `salaries` and `restaurants`.
3. Use Discover to explore the data.
4. Build visualizations such as:
   - Salary distributions
   - Average restaurant ratings per city
   - Correlation between salaries and restaurant prices
5. Save the visualizations in a dashboard.

### Cleanup
To stop and remove the containers:
```sh
docker-compose down
```

### Notes
- Ensure Elasticsearch is running before making requests.
- Modify queries as needed for deeper insights.

### Author
- Yazan Mizel

LINK FOR QUESTIONS
https://bi-labor.github.io/es-mssql/elasticsearch/

