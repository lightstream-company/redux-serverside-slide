### CQRS

 - Command Query Responsibility Segregation
 - Principe d'architecture assez simple

 <img src="slides/img/cqrs-principle.png" alt="data-centric VS domain-centric architecture" style="height:300px;"/>


### CQRS

 classe `CustomerService`

 ```c#
 void MakeCustomerPreferred(CustomerId)
 Customer GetCustomer(CustomerId)
 CustomerSet GetCustomersWithName(Name)
 CustomerSet GetPreferredCustomers()
 void ChangeCustomerLocale(CustomerId, NewLocale)
 void CreateCustomer(Customer)
 void EditCustomerDetails(CustomerDetails)
 ```


### CQRS

 classe `CustomerWriteService`

 ```c#
 void MakeCustomerPreferred(CustomerId)
 void ChangeCustomerLocale(CustomerId, NewLocale)
 void CreateCustomer(Customer)
 void EditCustomerDetails(CustomerDetails)
 ```

 classe `CustomerReadService`

 ```c#
 Customer GetCustomer(CustomerId)
 CustomerSet GetCustomersWithName(Name)
 CustomerSet GetPreferredCustomers()
 ```
<span style="font-size:12pt;">_source: http://codebetter.com/gregyoung/2010/02/16/cqrs-task-based-uis-event-sourcing-agh/_</span>


### CQRS

 - Enjeux différents
    - Queries : indexation, aggrégation, projection
    - Commands : consistance

 - On peut aussi séparer
    - Les modèles : normalisation VS dénormalisation
    - Les sources de données

 - Pattern très intéressant pour scaler
