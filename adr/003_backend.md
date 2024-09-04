# Backend

| status  | context                                                                                                                                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Draft | The backend framework should seamlessly integrate with the chosen frontend (Next.js) while offering strong performance and scalability. It should also provide a solid foundation for API development. |

## Evaluation criteria

- Integration with Frontend
- Performance
- Ecosystem + Libraries

## Options Considered

- **NextJS**
  - Pros
    - Optimal integration with frontend
    - No abstraction through APIs for the frontend
    - Good ecosystem
  - Cons
    - Not optimal for long running tasks (May require additional backend service)
- **NestJS**
  - Pros
    - Modular Architecture for extendability
    - Good scalability
    - Integrated support for micro services
    - Good ecosystem
  - Cons
    - Requires abstraction through APIs
    - No seamless integration with frontend
- **Django**
  - Pros
    - Good ecosystem
    - Included ORM + Admin interface
  - Cons
    - Different programming language adds complexity
    - Python might not have optimal performance
    - Requires abstraction through APIs
    - No seamless integration with frontend
- **Laravel**
  - Pros
    - Highly popular
    - Support for most backend needs out of the box
  - Cons
    - Different programming language adds complexity
    - Requires abstraction through APIs
    - No seamless integration with frontend

## Decision - NextJS

Since it was already chosen for the frontend it is easier to integrate it as the backend as well. There is no need to create separate API endpoints to get data into the frontend although that is also possible.

## Future Considerations

Since NextJS is optimized for handling short lived requests and responding to requests immediately it is not optimal for eventual long running tasks. The project requirements currently do not require those, but if this changes a separate backend would be needed to be integrated as a service. In this scenario **NestJS** would be a good choice for that.
