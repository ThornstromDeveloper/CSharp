# C#

## LINQ - Language Integrated Query

### Set source and range

Start with from clause to introduce source (customers) and range (cust)

`var queryAllCustomers = from cust in customers select cust;`

### Filtering

Returns customers from "London":

`var queryLondonCustomers = from cust in customers where cust.City == "London" select cust;`

Returns customers from "London" and named "Devon":

`var queryLondonCustomers = from cust in customers where cust.City == "London" && cust.Name == "Devon" select cust;`
