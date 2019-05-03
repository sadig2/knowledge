There are two ways to register the driver with the DriverManager . One way is to load
the driver class in your Java program. For example,
Class.forName("org.postgresql.Driver"); // force loading of driver class
This statement causes the driver class to be loaded, thereby executing a static
initializer that registers the driver.
Alternatively, you can set the jdbc.drivers property. You can specify the property
with a command-line argument, such as
java -Djdbc.drivers=org.postgresql.Driver ProgramName
Or, your application can set the system property with a call such as
System.setProperty("jdbc.drivers", "org.postgresql.Driver");
You can also supply multiple drivers; separate them with colons, for example
org.postgresql.Driver:org.apache.derby.jdbc.ClientDriver
