# 10/25/21: Serialization and Sorting

- Data can be **serialized** in one environment/programming language and sent to another environment/language, where it is **deserialized**
- Need to notice what parts of the data are crucial so others can deserialize it; similar to interfaces, there must be a mutual agreement

## JSON
- JSON is popularly used in serializing
- In our MP, we use JSON to pass data from **server** to **client** (which would normally be running on two different machines, communicating over a network)
- Every JSON object is enclosed in { ... } and arrays are enclosed in [ ... ]
- Numeric literals are not serialized but everything else must be in quotes 

## Data Flow in our Andriod Application
CSV file with restaurant information -> Server file under the network folder -> Load data into client via JSON -> When app launches, it loads the list of restaurants as a JSON String 

## Additional MP Tips
- Change and run test suites, instead of grader, to check for errors 
- Zero in on a single test suite at a time: green play button