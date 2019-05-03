lamiyapanahova@gmail.com; Competence-12
ale


Files.createDirectories(Paths.get("hmee", "second"));
Files.createFile(Paths.get("hmee","second","myfile"));

InputStream inputStream = new FileInputStream("database.properties");
  InputStreamReader  inputStreamReader = new InputStreamReader(inputStream);
  BufferedReader bufferedReader = new BufferedReader(inputStreamReader);



InputStream inputStream  = new FileInputStream("database.properties");
properties.load(inputStream);
inputStream.close();
