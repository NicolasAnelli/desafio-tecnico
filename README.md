# CEP search service

CEP search service is a Java service build in Springboot framework for dealing with CEP necessities when you only have a code, and want some more info about the fully address.

## Structure

The project has a layer structured API, that could be splitted into 3 main parts, web layer, application layer and domain layer;

### Web layer

The web layer is in **desafio.web package**. This is where all the controllers should be created. This package is responsable for handling all the web interactions

### Application layer

The application is in **desafio.application package**. This is where happens some convertions between the outer layers (as web layer), and the domain layer. This package is responsable for converting some data to be exposed to API, here would be a nice place for handling with exception for logging them.

### Domain layer

The domain layer is in **desafio.domain package**. This is where business logic are concentred. This layer usually do the business validations and data processing. This layer is stricted closed, and can only be access by the exposed method for the public services. This is important to prevent any wrong development.

