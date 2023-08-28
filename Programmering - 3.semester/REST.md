# What is REST?

REST (Representational State Transfer) is an architectural style for building distributed systems and web services. It was first introduced in 2000 by Roy Fielding in his doctoral dissertation. At a high level, REST aims to create web services and APIs that have desirable properties such as performance, scalability, simplicity, modifiability, visibility, portability and reliability.

The key goals of REST include:

- Simplicity of interfaces
- Scalability of architecture
- Modifiability of components
- Visibility of communication between components
- Portability across a wide range of platforms
- Reliability and stability of operation

To achieve these goals, REST defines a set of constraints and principles for building web services:

- Client-server separation of concerns
- Statelessness of requests
- Use of a uniform interface (HTTP)
- Access to resources via URIs
- Use of hypermedia for representing resources
- Self-descriptiveness of messages
- Caching of resources where applicable

By applying these constraints, REST aims to create web services and APIs that are lightweight, flexible, loosely coupled and have good performance. The restrictions force the creation of components and interfaces that can evolve independently over time and can be implemented on a wide variety of platforms.


Overall, the REST architectural style aims to provide a standard way of designing web services that take advantage of existing protocols and features of the internet's interconnected infrastructure to be scalable, flexible and reliable.



The key principles of REST include:

## Client-Server

There should be a separation between the client and the server. The client handles the user interface and user interactions, while the server handles the data storage,business logic, and data access. The client and server can evolve and scale independently from each other.

## Statelessness 

The server does not store any client state. Each request from the client contains all the information required by the server to understand and respond to the request. The server does not rely on stored context from prior requests.

## Cacheability

Responses from the server must indicate if they are cacheable or not. This allows client caching to improve performance and scalability.

## Uniform Interface 

There is a uniform way of interacting with server resources through the interface. This simplifies the architecture and enables independent evolution of client and server components.

## Layered System

The system architecture is composed of hierarchical layers, with each layer having a specific role. This improves flexibility and enables load balancing.

## Code on Demand (optional)

The server can provide executable code or scripts for the client to execute in its context. This enables further flexibility and customization.

By following these constraints and principles, REST aims to create web services and APIs that have good performance, reliability, and scalability. The restrictions force the creation of flexible and loosely coupled systems.
