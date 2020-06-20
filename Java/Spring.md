# Spring - Java


## RESTful APIs

In Spring's approach to to building RESTful web services, HTTP requests are handled by a controller. These components are identified by the `@RestController` annotation. This annotation marks the class as a controller where every method returns a domain object instead of a view. 

The `@GetMapping` annotation ensures that HTTP GET requests are mapped to a certain method.

The `@PostMapping` annotation ensures that HTTP POST requests are mapped to a certain method.

There is also the `@RequestMapping` annotation that they both derive from. 

`@RequestParam` binds the value of a query string parameter to the parameter of a certain method. You can set a default value for the request param.

## Data Transfer Object (DTO)

A DTO is an object that carries data between processes.

When you are working with a remote interface, each call can be expensive. In order to solve this, you need to reduce the number of calls. This is solved by creating a data transfer object that can hold all the data for the call, like a JSON object.

## Data Access Object (DAO)

A DAO abstracts and encapsulates all access to a data source. 

The DAO manages the connection with the data source to obtain and store data. 

The DAO abstracts the underlying data access implementation for the service objects to enable transparent access to the data source. The service also delegates data load and store operations to the DAO. 

## Services

Service objects are doing the work that the application needs to do for the domain you're working with. It involves calculations based on inputs and stored data.