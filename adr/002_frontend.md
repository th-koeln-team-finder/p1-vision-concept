# Frontend

| status  | context                                                                                                                                                                                           |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Draft | The frontend framework should offer strong performance, including server-side rendering (SSR) capabilities, and provide a smooth developer experience. It should also have a robust ecosystem for components and libraries, supporting the creation of dynamic, responsive UIs. |

## Evaluation criteria

- Developer Experience
- Performance
- Ecosystem + Libraries

## Options Considered

- **NextJS (React)**
  - Pros
    - Big ecosystem with many libraries
    - Advanced SSR with streaming
    - Widely used
  - Cons
    - Often times dependent on many libraries
- **SvelteKit (Svelte)**
  - Pros
    - Highly performant, minimal runtime overhead
    - Lightweight
    - Easy to learn
  - Cons
    - Smaller ecosystem
    - Few large scale production examples
- **Nuxt (Vue)**
  - Pros
    - Good ecosystem (though not as big as React)
    - More widely used than SvelteKit
  - Cons
    - Less performant than Svelte
    - Fewer libraries available than React

## Decision - NextJS

React has the most robust ecosystem and advanced SSR features for good performance. The larger community and available libraries will reduce the time of development significantly.
