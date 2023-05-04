Post 2 - Serialization 1

As the last meeting was cancelled, I had enough time to add some extra code to the serialization github. I took some good notes on exactly what the serialization repo should look like.

The serializeToCSV and deserializeFromCSV method, as well as a prettyPrintToCSV method have been added, and I decided a class called car is what will be serialized. 

I looked into nio from https://www.baeldung.com/java-io-vs-nio, and I believe I was able to implement it using Files.write(Paths.get(fileName), writeData.getBytes()).

The reason why I chose a car class is because I feel that its class name conveys an "arbitrary" quality. An actual car class seems unlikely to be useful in a real world scenario, however it is often used as an example.

I also implemented some extra code in the serialization function that would allow the serialization of multiple cars, although that was not explicitly a part of the original task.

I'm still working with understanding GitHub. Dr. Bowring has been helpful whenever strange errors prevent me from pushing. I'm starting to understand the protocol I will be using for interactive with other users/collaborating on Tripoli.
