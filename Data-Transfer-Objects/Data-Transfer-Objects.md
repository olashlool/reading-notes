# Reading 16: Data Transfer Objects

## Create Data Transfer Objects (DTOs)

When web APIs expose database entities to the client, the client receives data that maps directly to your database tables. However that is not always a good idea. Sometimes you want to change the shape of the data that you send to the client. For example, you might want to:

- Remove circular references
- Hide particular properties that clients are not supposed to see
- Omit some properties in order to reduce payload size
- Flatten object graphs that contain nested objects, to make them more convenient for clients
- Avoid "over-posting" vulnerabilities
- Decouple your service layer from your database layer

To accomplish this you can define a data transfer object (DTO).

A DTO is an object that defines how the data will be sent over the network.

## How to use Data Transfer Obejcts in ASP.NET Core 3.1

A Data Transfer Object (DTO) is usually an instance of a POCO (CLR object) class used as a container to encapsulate data and pass it from one layer of the application to another. You would typically find DTOs being used in the service layer to return daya back to the presentation layer. The biggest advantage of using DTOs is decoupling clients from you internal data structures.
