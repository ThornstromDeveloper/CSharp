# C#

## LINQ - Language Integrated Query

### Query expression

#### Set source and range

Start with from clause to introduce source (customers) and range (cust)

```
var queryAllCustomers = from cust in customers select cust;
```

### Filtering

Returns customers from "London":

```
var queryLondonCustomers = from cust in customers where cust.City == "London" select cust;
```

Returns customers from "London" and named "Devon":

```
var queryLondonCustomers = from cust in customers where cust.City == "London" && cust.Name == "Devon" select cust;
```

### Method syntax

#### Count() - Count occurences in list

Returns the amount of numbers in 'numbers' below 3 and above 7 (5):

```
List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
var numCount = numbers.Where(n => n < 3 || n > 7).Count();
```

#### ToList() - Return occurences in list

Returns the occurences of numbers in 'numbers' below 3 and above 7 (5):

```
List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
var numList = numbers.Where(n => n < 3 || n > 7).ToList();
```

### Query expression with method syntax

#### Count() - Count occurences in list

Returns the amount of numbers in numbers below 3 and above 7 (5):

```
List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
int numCount = (from num in numbers where num < 3 || num > 7 select num).Count();
```

#### ToList() - Return occurences in list

Returns the occurences of numbers in 'numbers' below 3 and above 7 (5):

```
List<int> numbers = new List<int>() { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
int numList = (from num in numbers where num < 3 || num > 7 select num).ToList();
```

## String properties

#### String.Length

Definition:
```
public int Length { get; }
```

Example:
```
string str = "abcdefg";
int length = str.Length;
```

'length' will be 7

## String methods

#### String.Contains

Check whether the substring occurs within a given string or not.

Definition:
```
public bool Contains(string str)
```

Example:
```
List<string> my_list = new List<string>() { 
        "This is my Dog", 
        "Name of my Dog is Robin", 
        "This is my Cat", 
        "Name of the cat is Mewmew"
}; 

var res = my_list.Where(a => a.Contains("Dog")); 
```

'res' will have the strings: 'This is my Dog' and 'Name of my Dog is Robin'

#### String.Join

Concatenates all the elements of a string array, using the specified separator between each element.

```
string[] words = { "one", "two", "three" };
var result = string.Join(",", words);
```

'result' will be 'one,two,three'
