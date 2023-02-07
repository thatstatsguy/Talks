Video Source: https://www.youtube.com/watch?v=fxZhU8b_cjk
Github repo: https://github.com/cecilphillip/ZeroToHeroDaprCon
Microsoft documentation: https://learn.microsoft.com/en-us/dotnet/architecture/dapr-for-net-developers/

Difficulties in Microservices
- service discovery
    - what's available 
    - where are they?
    - what's their health?
- limited language support for speicific tools
- platform considerations (e.g. can we deploy to linux with the given tools we have?)

## DAPR = distributed application runtime
- programming language, host agnostic runtime
- open source
- dapr provides a layer of abstractions for various objectives
- objectives can be broken down into various microservice building blocks
- building blocks are used in dapr for specific use cases e.g. service discovery, state management.
- dapper uses http and grpc in the background, as long as programming language supports this you're good.

# Dapr demo
- running application with dapr requires a unique id
- run application on the same port as dapper in the case as of running an api
- localhost:8080 is dapper dashboard for running the different options
- dahboard shows different components that are running
- dapr operates a sidecar model
    - for each application running, we'll have a separate instance of dapper running next to it
- these apps communicate via grpc/http via the dapr api
- dapper components
    - underneath each building block there's several components you can use to integrate
    - e.g. under state store building block you may want to use firebase component or redis component


- concrete implementations have no reference to dapper e.g. in the csproj file
- in compose file - you'll be specifying several dapr services to run in the side car format.
- Cloud events is what dapr uses for pub sub events
