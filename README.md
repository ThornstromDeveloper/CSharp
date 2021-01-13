# C#

## LINQ - Language Integrated Query

### Query expression

#### Set source and range

Start with from clause to introduce source (customers) and range (cust)

`var queryAllCustomers = from cust in customers select cust;`

### Filtering

Returns customers from "London":

`var queryLondonCustomers = from cust in customers where cust.City == "London" select cust;`

Returns customers from "London" and named "Devon":

`var queryLondonCustomers = from cust in customers where cust.City == "London" && cust.Name == "Devon" select cust;`

### Method syntax

#### Count occurences in list

Returns the amount of numbers in numbers below 3 and above 7 (5):

`List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };`
`var numCount = numbers.Where(n => n < 3 || n > 7).Count();`

### Query expression with method syntax

#### Count occurences in list

Returns the amount of numbers in numbers below 3 and above 7 (5):

`List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };`
`int numCount1 = (from num in numbers where num < 3 || num > 7 select num).Count();`
