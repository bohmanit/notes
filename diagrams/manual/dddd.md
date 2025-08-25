För en ny utvecklare som målgrupp:


säk kontroller
qa konstroller
compliance kontroller
prestanda
continuous delivery som princip, inte deployment

gitops som princip princip

komponent->system->


Ingångsvärden kan vara säkerhet, comliance eller kvalitativa krav.
Utgång: ledare kan läsa på och implementera våra principer.


devscops kringlan.


ta devsecops kringlan och platta ut. lägg dom andra blocken ovanpå.


vad & varför inte hur....



devsecops
---------
flöde, vad
---------
cicd principer


----------------------------

Core Principles:
- We always communicate artefacts through releases, never directly between repositories.


Principles and Guidelines for implementing CICD:
Description: This is where single components/applications reside, where they are built, where unit tests is run.
- In the Component repository / CI step:
    - we publish docker image
    - web publish the helm chart describing how to run the application by default with default values provided, that others may use
    - helm chart is always bumped with a patch version when the application is changed
    - changes to the helm chart itself is denoted by using semantic versioning when making changes to the chart
    - changes the application is always denoted with semantic versioning
    - when artefacts such as images or openapi specs is updated, then a release should be created
    - no direct integration with other repositories should be used, instead a pull based or event based approach should be used, this is to avoid a brittle system that is hard to evolve over time
    
In the System/Configuration repository:
Description: this is where system archetypes is defined, like client, partner integration or microservice.
- In the System repository:
    - we publish artefacts that we want to share with others, example: OpenAPI specifications
    - we manage the version of the whole system
    - the system is always packaged as an umbrella chart with dependand charts for components






