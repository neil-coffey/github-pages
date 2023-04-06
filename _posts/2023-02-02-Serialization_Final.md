This week, I made some serious changes to the Serialization repository. I managed to make it such that when I am deserializing, I remove the entry from the file that I am deserializing and close. This is because the serialization function only can deserialize one object, so if there are multiple objects in a file, this simple method can allow all of them to be deserialized. There are potential issues if for example the program crashed before they could reserialize, but we assume that this won't happen.

I also added more vehicle classes as instructed. I created a vehicle interface and added a vehicle class that implements that interface (and made the car class implement the interface). Through this I learned the important lesson that when you are declaring variables that have some sort of super class, it is better to be more general on the declaration and more specific on the instantiation. 

I got rid of the Serialization/Deserialization functions in their own classes, as this was an old discussion that I may have misunderstood. Really, they were supposed to be a part of the actual class that I am serializing/deserializing.

I also started to add a comparator. I ran into issues since its been awhile since I was doing work in Java, and I did not realize there's a difference between comparator and comparable. This left me questioning which one I had used prior, and going back through my old code - only to find that I had implemented comparable. This left me more stuck than I was hoping, but I still was able to get it implemented without errors at least, although it does not perform exactly the way it should.

The blog also has been started, although I'm sure figuring out the next steps for that will take some time.
