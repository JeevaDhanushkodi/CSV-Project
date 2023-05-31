# CSV-Project

Project has controller, service, serviceimpl and repo layers.

we accept file as a input and process it to store the order data based on country.
With the help of csvutils, read the file and converted the columns into object and stored into the DB.
Flow goes like below:
controller->service->serviceimpl->repository.
service is used here to achieve abstraction, as it's an interface and has only the metod declaration and not definition. whereas service implementation class has all the deifinitoins.
Handled the exceptions using try and catch blocks. Thrown the exception from service layers and catched it in the controller and show proper message to the user. 

used lombok repo to make use of more annotations like @Data, @getter, @setter, @noargsconstructor etc.,
used mongodb in the backend to store the data. 
In the service Layer after reading the data from csv file, checking if a specific country code is present, then based on that the respective country ie being set. Just for example
have added only 2 cases. except country all the other fields are set using the "CsvUtils.read" method, which converts given file into the entity as given in parameter.

written junit test cases using junit and mockito. mocked the services and repos and input file to check the response. 

Added Java doc in respective methods and provided proper method explanation and its usages.
