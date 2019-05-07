# GRPC-HelloWorld

This is a Hello World for GRPC, using java and maven. <br/>
The java files are in the test folder, basically testing if the pom is working properly or not. <br/>
In some projects adding this depenencies will cause the compilation or running tests fail. For example if there is Guava depenency conflict between multiple plugins, the test will fail, not being able to run the test. 


The pom contains the changes needed for creating a GRPC project. 

The test folder contains a helloworld test. 

# To Run the test via maven:
clone this repo. 

To compile and run tests: 
```mvn clean install```

You should see the test running like this:
```
Running io.grpc.examples.helloworld.HelloWorldServerTest
```

# To run the client/server manually:
To run the server: 
```
mvn test-compile exec:java -Dexec.mainClass="io.grpc.examples.helloworld.HelloWorldServer" -Dexec.classpathScope="test"
```

To run the client in another tab: 
```
mvn test-compile exec:java -Dexec.mainClass="io.grpc.examples.helloworld.HelloWorldClient" -Dexec.classpathScope="test"
```


