
DBT Modern Data Stack .


## 1- Pipeline documentation

## 2- Database Tables Can  Quality tested easily 
  - SODA SQL Integeration 
  - GreatExpectations Integration

## 3- Database tables can be documented easily 
- Documenting table names , Columns names & description 

## 4- Whole piplelines inlined via Microservice architecture

## 5- Can be integerated into Modern CI/CD Pipeline.

## 6- Can version controlled Easily  

## 7- Code organisation - organizing SQL transformation pipelines


## 8- Orchestrate &  scheduled workflow
 - DBT Jobs compatible with following  orchestration frameworks : ```prefect``` and ```Airflow```

---
## Unit test Example.
Example :
```YML
version: 2

models:
  - name: orders
    columns:
      - name: order_id
        tests:
          - not_null

```
---
## Each Table (Model ) Must be Tested/Documented 
### Below Example of `events` table been tested and documented 
```yml
version: 2

models:
  - name: events
    description: This table contains clickstream events from the marketing website

    columns:
      - name: event_id
        description: This is a unique identifier for the event
        tests:
          - unique
          - not_null

      - name: user-id
        quote: true
        description: The user who performed the event
        tests:
          - not_null

```
---
## All dbt projects should be version controled 




 