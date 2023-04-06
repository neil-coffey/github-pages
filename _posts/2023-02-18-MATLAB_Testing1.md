This has been a wild 2 weeks compared to what I was doing previously. Serialization was done, so I was tasked with beginning on the Tripoli GitHub. Since this is a Test-Driven-Development course, I was tasked with working on testing.

For right now, I am looking primarily at the MatLabTest.java file, where there are already tests for all of the MATLAB re-implementations for Tripoli. Although there are already tests, most of them test between 1 and a handful of cases, not including any edge cases. Dr. Bowring wants me to make these tests more robust.

The first week, I went and added some edge cases to most of the tests, which are cases that may not represent the majority of cases, but must therefore be tested to verify that even in extreme or odd scenarios, the code still works. I was thinking that adding some edge cases would be sufficient, but then just the day before the meeting with Dr. Bowring I realized 2 things:

We are developing this for MATLAB, so we must be sure that each case (and edge case) provides almost exactly the same output as MATLAB.

The fewer cases that are tested, the less convincing the tests may seem to a third party (and to a lesser extent, to the developer).

This led to 2 further bits of reasoning:

Since we need to test each function in MATLAB with a particular input first, then test the Java function, it will be tedious and inefficient to test each function manually for several cases.

One case where only a few tests may fall short is when considering rounding errors that happen relatively infrequently, but frequently enough to become an issue.

The second bit of reasoning occurred only after I had developed a few tests. What I found was that different Java implementations had differing probabilities of encountering a rounding error at different decimal places. How I discovered this directly relates to the next step of the testing process, which was to automate MATLAB/Java testing by serializing matrices from MATLAB including inputs and answers and deserializing them in Java. This would allow me to test hundreds or even thousands of cases, including randomly generated edge cases, to reliably identify errors at a level beyond just a few simple cases. 

At first, I thought that while this was a great idea, since the math was what was being tested, only a few test cases should be enough, since if the math was not working, the probability of getting the function output that matched the correct answer was going to be very low to begin with. But, after implementing one case of this, an interesting result was found -

Not every Java implementation of the MATLAB functions was accurate to the same number of significant figures. In fact, this number differed a lot from function to function, and without testing dozens of cases, the number of sigfigs that worked for a few cases could be 1 or 2 greater than the true number that was found after testing several more. This gave newfound purpose to the serialization of results from MATLAB. Not only could I test hundreds of cases, including edge cases, essentially proving beyond all doubt that the Java functions really work, but I also could verify the accuracy of these functions to a certain decimal point. 

So, this week I did as many as I could. I serialized the results from around 5 to 7 MATLAB functions and wrote some functions to import them and deserialize them in Java. There are quite a few functions with inputs that are harder to serialize, but we will discuss this in our next meeting.
