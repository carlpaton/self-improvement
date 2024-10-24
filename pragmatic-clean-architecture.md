# Clean Architecture Fundamentals

## Architectural principles & Design principles

### Architectural Principles

Architectural principles are the rules and guidelines that drive a specific software architecture, these are highlevel qualities inforced by design, they include but are not limited to

- Maintainablity
- Testability
- Loose coupling

### Design principles

These should be guiding your software development process

- **Separation of concearns**; 
  - here we would separate the concearns of the core domain from the external dependencies such as `database` and `user interface`
- **Encapsulation**;
  - focus on hiding information from the outer components, also isolating your components from influence of outer components
  - see https://carlpaton.github.io/2018/03/pillars-of-object-oriented-programming-oop/
- **Dependency inversion**;
  - components depend on abstractions at compile time and implementations at runtime
  - see https://carlpaton.github.io/2018/04/dependency-inversion-principle-dip/
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
