# C#

## LINQ - Language Integrated Query

### Set source and range

Start with from clause to introduce source (customers) and range (cust)

`var queryAllCustomers = from cust in customers select cust;`

### Filtering

`var queryLondonCustomers = from cust in customers where cust.City == "London" select cust;`
