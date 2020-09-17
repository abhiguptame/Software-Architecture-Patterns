# Software Architecture Patterns:

## Patterns in Software:
- Solution to common problem 
- Components and interactions

## Design Pattern vs Architecture Patterns:

| Design Pattern | Architecture Patterns |
|----------------|-----------------------|
| Small amount of components | Defines a significant part of the application |
| Part of a larger application | Many components and mostly paradigm independent |

## Categories of patterns:
1. Application Landscape
2. Application Structure 
3. User Interface

## 1. Application Landscape Pattern:
- Single application to the end user
- Multiple applications behind the scenes possible

### Application Landscape Pattern Types:
- Monolith
- N-tier
- Service-oriented
- Microservices
- Serverless
- Peer-to-peer

#### Monolith:
- Single Executable 

| Advantages | Disadvantages |
|------------|---------------|
| Easy to understand, implement, and test | Tight coupling |
| Easy deployment | Easily leads to complex code |
| Ideal for limited scope | One size fits all for every subdomain |

#### N-Tier:
- Multiple tiers
- Tier performs specific task
- Tiers can be physically separated
- Tiers aren't layers
- Technical boundaries

| Advantages | Disadvantages |
|------------|---------------|
| Independent development, Scalability | Change ripple through tiers |

#### Service-oriented
- Multiple services
- Each service is a business activity
- Service composability
- Contract standardization
- Enterprise service bus

| Advantages | Disadvantages |
|------------|---------------|
| Services are loosely coupled | Reduced agility and team autonomy |
| Scalability | Costly |
| No duplication of functionality | Many differing views |

#### Microservices:
- Multiple Services
- Each service is a business activity
- Teams run the service
- No logic-heavy enterprise service bus
- Maximum automation


| Advantages | Disadvantages |
|------------|---------------|
| Services are loosely coupled and easily scalable | Boundaries not always clear |
| Increased agility, Reliability, Designed to handle failures | Communication patterns can become complex |


## 2. Application Structure Patterns:
- Single executable
- Can be part of a larger application landscape

### Application Structure Pattern Types:
- Layered
- Microkernel
- Command Query Responsibility Segregation (CQRS)
- Event sourcing
- Command Query Responsibility Segregation and Event sourcing combined

## 3. User Interface Patterns:
- Model-view-controller (MVC)
- Model-view-presenter (MVP)
- Model-view-viewmodel (MVVM)






