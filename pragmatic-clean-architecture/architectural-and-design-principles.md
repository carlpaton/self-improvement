## Architectural & Design principles

### Architectural Principles

Architectural principles are the rules and guidelines that drive a specific software architecture, these are highlevel qualities inforced by design, they include but are not limited to

- Maintainablity
- Testability
- Loose coupling

### Design principles

These should be guiding your software development process

- **Separation of concearns (SRP)**; 
  - here we would separate the concearns of the core domain from the external dependencies such as `database` and `user interface`
- **Encapsulation**;
  - focus on hiding information from the outer components, also isolating your components from influence of outer components
  - see https://carlpaton.github.io/2018/03/pillars-of-object-oriented-programming-oop/
- **Dependency inversion (DIP)**;
  - components depend on abstractions at compile time and implementations at runtime
  - dependancies flow inwards, the inner layers define abstractions/interfaces, the outer layers implement them
  - this means the inner layers will not reference the outer layers
  - see https://carlpaton.github.io/2018/04/dependency-inversion-principle-dip/

 ![image](https://github.com/user-attachments/assets/2c74010f-cfc5-4707-9a5a-b59458a77b83)


- **Explicit dependencies**;
  - components should be honest about their dependencies that they require to function properly, this improves the stability of your components
- **Single responsibility**;
  - components should have one responsability only and only one reason to change which promotes granular design of your components improving stability
  - see https://carlpaton.github.io/2018/05/single-responsibility-principle-srp/
- **DRY**;
  - Dont Repeat Yourself which focuse on reducing duplication in your code by encapsulating repetitive behavior
- **Persistence ignorance**;
  - concearned with how you design your domain entities, done in such a way that it doesnt matter the `persistence mechanism` technology under the hood
  - so it doesnt matter if you use a `SQL Database`, `Document Database` or a `Key Value Store`, these decisions should not affect how you model domain entities
- **Bounded contexts**;
  - term from Domain Driven Design, the Bounded contexts is a conseptual model grouping related entities and behaviours together
  - at a bare minimum your application should be a single bounded context, in some cases you would have more bounded contexts in a single application
  - see https://carlpaton.github.io/2020/04/domain-driven-design/

### Domain Centric Architecture

Clean architecture is not a new concept, its an evolution of `Domain Centric Architecture` which would have the core domain encapsulating main business logic / rules. This then has supporting components such as presentation and infastructure. This is a domain centric approach to organising dependencies.

Simliar architectures that you may have heard of are which all revolve around the same idea of having a rich application core (the domain) which contains all business logic

- Onion architecture
- Hexagonal architecture

![image](https://github.com/user-attachments/assets/0cc23b09-4ab5-4ceb-b94a-2dfa3dac87f3)

### When is Clean Architecture right for me

If you have been coding for a while you will know that its not a one size fits all, sometimes having too many abstractions make your code more complex than it needs to be. Some general fit use cases of `Clean Architecture` could be as follows

- **Domain-Driven Design**;
  - DDD fits naturally into the `domain layer` of Clean Architecture, its the central piece of the architecture
- **Complex business logic**;
  - When solving complex business logic, here Clean Architecture shines in isolating your business logic in the domain layer
  - Through the Use Cases of the application layer
- **High testability**;
  - Clean Architecture is highly testable because of the way the components are designed, they follow SRP and DIP which both help a lot to improve testability
- **Software architecture to enforce design policies**;
  - In larger teams Clean Architecture is a good choice
