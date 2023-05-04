For this week, I added new resource files and fixed several of the tests. The files that already existed only had about 10 test cases in them, and not all of them had edge cases (as a combination of random chance and poor implementation). 

I made sure this week that all of the files have 100+ test cases and that each of them implement at least edge cases where matrices of zeros are multiplied together. 

This week is also clearly demonstrates "testing vs. debugging". These are not the same, and while testing may identify that there is a bug, it does not directly identify what the bug is or what caused it. In order to find why some of the tests are failing, I need to go into the code. This will lead me to finding rounding errors, or even errors in the original functions.

There were several fixes that I added to the code. For example, kron (as in the kronecker product) was sometimes working, but not always. I identified that this was because I was improperly assigning the edge case matrix to the wrong variable in MATLAB. Perhaps I should make all of the MATLAB code public in a new repository where these functions can be improved later, after making sure they all work.

I also ran into some trouble with some of the code. I noticed that rDivide does not seem to be working properly. Regardless, I flipped the MATLAB parameter order to reflect the specific implementation for this code, so in this case it works just fine and all the tests pass, although for some reason the number of sigfigs is very low. The function is quite simple, so there does not seem to be any obvious errors that would point to why the sigfigs are so low, but I assume that there must be some sort of logical explanation. 

Since I have just figured out that it would make sense to keep any additional parameters in an additional matrix and just manually pull out the values, now I am able to properly test some of the other functions that were using hardcoded values, such as find. Overall, I now have 7 or 8 functions fully tested.
