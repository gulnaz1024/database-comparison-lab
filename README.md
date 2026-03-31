# MongoDB vs Cassandra Lab  
## Two Databases Walk Into a Bar.

This lab compares MongoDB (document store) and Cassandra (wide-column store) using the same dataset.

---

## Project Files

- `docker-compose.yml` — runs MongoDB and Cassandra  
- `lab.ipynb` — contains all queries and outputs  
- `README.md` — reflection answers  

## Reflection
### 1. Schema
MongoDB is better when data may change often or when the structure is flexible, because it does not need a schema first. Cassandra is better when the structure is known in advance and fast large-scale reads/writes are needed.

### 2. Query limitation
The error said that Cassandra could not execute the query because it might require data filtering with unpredictable performance. Cassandra restricts this because tables are designed around the partition key and clustering key, so queries must follow that design.

### 3. Use case
MongoDB would be a good choice for an online store catalog where products may have different fields. Cassandra would be a good choice for a system with huge amounts of transaction or log data where fast distributed performance is important.


## How to Run

Start containers:

```bash
docker-compose up -d
