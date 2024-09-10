# Backend

| status  | context                                                                                                                                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Draft | The project requires a file storage solution that is cost-effective and easy to manage in its early stages, with the potential to scale as the project grows. The solution should also offer compatibility with widely-used cloud storage services to facilitate future migration if necessary. |

## Evaluation criteria

- Scalability
- Ease of Use
- Cost
- Performance

## Options Considered

- **Amazon S3**
  - Pros
    - Industry standard for file storage
    - Highly scalable
    - Strong security features
    - Globally distributed
  - Cons
    - Costly
    - Required to store data with Amazon
    - Complex setup for smaller applications
- **MinIO**
  - Pros
    - Lightweight
    - Easy Self deployment
    - S3 API Compatible
    - Cost effective
  - Cons
    - Requires self management
    - No global distribution
    - Might need to scale to S3
- **Google Cloud Storage**
  - Pros
    - Good scalability
    - Good performance
    - Globally distributed
  - Cons
    - Required to store data with Google
    - Costly
    - Complex setup

## Decision - MinIO

It can easily be used during development and self deployed in the initial phases of the project. Once the service needs to scale and requires more maintenance the project could move to Amazon S3 as the more mature solution with little effort if needed.
