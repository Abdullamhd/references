
DBT Modern Data Stack .  

---
## Each Table have to Unit tested 
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
## All dbt projects should be managed in version control
