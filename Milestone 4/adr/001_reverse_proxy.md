# Reverse Proxy

| status  | context                                                                                                                                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Draft | The website requires a reverse proxy to handle load balancing, SSL termination, and routing requests to the appropriate backend services. This will help ensure scalability, security, and flexibility. |

## Evaluation criteria

- Ease of Configuration
- Performance
- SSL Management
- Simplicity
- Security

## Options Considered

- **Nginx**
  - Pros
    - High performance
    - Mature
    - Highly configurable
    - Widely used
  - Cons
    - High complexity
    - Time consuming configuration
    - SSL hard to handle properly
- **Caddy**
  - Pros
    - Easy configuration
    - Automatic encryption with Lets Encrypt
    - Strong security defaults
    - Good for small to medium sized applications
  - Cons
    - Small community
    - Fewer advanced features
- **Treafik**
  - Pros
    - Good for dynamic environments
    - Automatic SSL configuration with Lets Encrypt
    - Integration into Kubernetes
  - Cons
    - Complicated configuration
    - Might not utilize most of the features

## Decision - Caddy

The application has no need for complex reverse proxy logic, the focus of development should be in the application and not the proper proxy set up. Caddy not only strikes with its simplicity, but also its security features such as automatic SSL configuration.
