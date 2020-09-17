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

#### Serverless:
- Backend as a service
- Function as a service

| Advantages | Disadvantages |
|------------|---------------|
| Scaling | Libraries supports are Vendor Dependent |
| Reduced Costs | Cold Start |

#### Peer-to-peer:
- No central server
- No constant connection
- Dynamically discoverable

| Advantages | Disadvantages |
|------------|---------------|
| Sharing Resources | Possible security issues |
| Reduced Costs | Only for specific scenarios |
| Scaling | Nontrivial to code |

## 2. Application Structure Patterns:
- Single executable
- Can be part of a larger application landscape

### Application Structure Pattern Types:
- Layered
- Microkernel
- Command Query Responsibility Segregation (CQRS)
- Event sourcing
- Command Query Responsibility Segregation and Event sourcing combined

#### Layered:
- Each layer have distinguish responsibility
- A layer called the layer below it

| Advantages | Disadvantages |
|------------|---------------|
| Well-known among developers | Can lead to monolithic applications |
| Easy yo organize | Need to write lots of code |

#### Microkernel:
- Also called plug-in pattern

##### User cases:
- Task schedular
- Workflow
- Data processing
- Browser extensions
- Graphic desiner app plugins

| Advantages | Disadvantages |
|------------|---------------|
| Flexibility | Core API might not fit future plugins |
| Clean Separation | Can the plugins be trusted?  |
| Separate teams possible | Not always clear what belongs in the core |
| Add and remove functionality at runtime | Version support with applications |

#### Command Query Responsibility Segregation (CQRS):
- Two models: read/query and write/command
- Allows for scenario-specific queries 
- Synchronization required
- Different from event sourcing

| Advantages | Disadvantages |
|------------|---------------|
| Simpler read queries | Added complexity |
| Faster and more scalable read queries | Learning curve |
| Easier to communicate with stakeholders | Possibilities of data inconsistencies and Eventual consistency |

#### Event sourcing:
- Store events instead of current state
- Event = something that happened in the past
- Rehydration or replay

| Advantages | Disadvantages |
|------------|---------------|
| Trace of events | Replay and external systems |
| Audit trail | Event structure changes |
| Business language and Event replay | Snapshots |

#### Command Query Responsibility Segregation and Event sourcing combined:
- Two different concepts
- Powerful combination

| Advantages | Disadvantages |
|------------|---------------|
| Simpler and faster queries | Added complexity |
| Scalable | Learning curve|
| Trace of events | Data inconsistencies |
| Audit trail and Business language | Event structure changes |

#### CQRS and/ or Event Sourcing:
- Not for simple domains
- Start with event sourcing 
- Add CQRS later

## 3. User Interface Patterns:
- Model-view-controller (MVC)
- Model-view-presenter (MVP)
- Model-view-viewmodel (MVVM)

### Model-View-Controller:

| Advantages | Disadvantages |
|------------|---------------|
| Separation of concerns | Controllers can become bloated |
| Parallel development | Different definitions |

#### Model-View-Presenter:

| Advantages | Disadvantages |
|------------|---------------|
| Great for desktop application | Presenters can become bloated |
| Separation of concerns and Testability | Desktop applications are less popular |

#### Model-View-Viewmodel:

| Advantages | Disadvantages |
|------------|---------------|
| Great for modern desktop and mobile applications | Overkill for simple user interfaces |
| Separation of concerns | More difficult to debug |
| Testability | Desktop applications are less popular |

#### MVC, MVP, and MVVM: Differences

| | MVC | MVP | MVVM |
|-|-----|-----|------|
| User Interaction Handled By | Controller | View | View |
| Code in UI (Code Behind) | Minimal | Yes | Minimal |
| View Aware of Moedl | Yes | Yes (Supervising Controller) No (Passive View) | No |
| Data Binding | Basic | Basic (Supervising Controller) No (Passive View) | Advanced |

#### MVC, MVP, and MVVM: Similarities
- Decoupling view and model
- Extra component in between
- Increased testability


