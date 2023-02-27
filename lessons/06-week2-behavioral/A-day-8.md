# Build a server 

1 Hour Exercise 

1.  Choose a programming language: Select a programming language that you are familiar with and can use to build a web server. Some popular options include Node.js, Python, Ruby, and Java. (Do not use a framework, it's okay to use light libraries)
    
2.  Create a server: Create a socket and bind it to a port (e.g., 4000) on localhost. Listen for incoming connections from clients.
    
3.  Implement the server endpoints: When a client connects to the server, read the request from the client and parse the request URL. If the URL is [http://localhost:4000/set?somekey=somevalue](http://localhost:4000/set?somekey=somevalue), store the key and value in memory. If the URL is [http://localhost:4000/get?key=somekey](http://localhost:4000/get?key=somekey), retrieve the value stored at the specified key and return it in the response.
    
4.  Create HTTP response: Create an HTTP response with the appropriate status code, headers, and body, based on the endpoint that was called and the data that was retrieved.
    
5.  Send the response: Send the response to the client over the socket connection.
    
6.  Save the data to a file: Implement a function that writes the data to a file each time a new key-value pair is added. You can start with simply appending each write to the file, and work on making it more efficient if you have time.

7.  Test the server: Use a web client such as Postman or curl to test the server endpoints and make sure they are working correctly.
    
8.  Test the file saving functionality: Test the file saving functionality by adding some key-value pairs and verifying that they are saved to the file.
    
9.  Optimize the file saving: If you have time, you can work on making the file saving more efficient. For example, you can use a database instead of a file, or implement a caching mechanism to reduce the number of writes to the file.
    
10.  Review your code: Review your code to make sure it is well-organized, readable, and follows best practices. Make sure to handle error cases such as invalid input, missing keys, and file write errors.
    
11.  Practice explaining your code: Practice explaining your code to someone else, as you may be asked to do so during your interview. Make sure you can explain the purpose of each function and how they work together to implement the desired functionality.