> Draw and illustrate 3-tier web architecture. [5M]
***
#### 3-tier web architecture diagram and explanation [3M]
In the 3-tier architecture, an application is usually split into three separate logical layers. Each of these layers has well defined interfaces. The layers in the 3-tier architecture are:
- Tier 1 (Presentation): Consists of a GUI to interact with the user.
- Tier 2 (Business Rules): Consists of the business logic. It represents the code that the user calls upon through the presentation layer to retrieve the data from the data layer.
- Tier 3 (Data): Contains the data access logic needed for the application.

Diagram
![Diagram](images/3_tier_architecture.png)

#### Advantages and Disadvantages [2M]
Advantages
- It is easier to modify or replace any tier without affecting the other tiers.
- Multiple user interfaces can be built and deployed without changing the application logic; provided it defines a clear interface to the presentation layer.
- Separating the application and database functionality means better load balancing.
- Adequate security policies can be enforced within the server tiers without hindering the clients.

Disadvantages
- It is more complex structure.
- More difficult to setup and maintain.
- The physical separation of the tiers may affect the performance.
