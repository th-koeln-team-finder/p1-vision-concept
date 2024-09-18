# Backend

| status  | context                                                                                                                                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Draft | The database should provide reliable data storage and retrieval, with strong support for data consistency and scalability. Given the project's nature, it should be easy to use and manage while offering flexibility in data modeling to support future needs. |

## Evaluation criteria

- Data Consistency
- Performance
- Ease of Use

## Options Considered

- **LibSQL (SQlite for server)**
  - Pros
    - Simple setup
    - Lightweight
    - Best Performance with Embedded Replicas
  - Cons
    - Relatively new
    - Smaller ecosystem
    - Might require managed environment since selfhosting might be complicated
- **MySQL**
  - Pros
    - Widely used
    - Good performance
  - Cons
    - Not as mature with handling unstructured JSON data
    - Prior issues with locking
- **PostgreSQL**
  - Pros
    - Widely used
    - Extended integration of complex SQL features
    - Support for unstructured JSON data
  - Cons
    - Might be overkill for smaller use cases
- **MongoDB**
  - Pros
    - Flexible schema since it is NoSQL
    - Built-in sharding
  - Cons
    - Only eventual consistency
    - Extensive planning of data modeling for best performance

## Decision - PostgresQL

It provides good performance and scalability as well as data consistency. It has many SQL features for more complex queries and supports unstructured data which might be required for storing whiteboard information.
