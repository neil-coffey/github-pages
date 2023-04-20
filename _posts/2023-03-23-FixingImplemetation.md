For this week, I actually have made some improvements to the real Tripoli code. From last week, I learned that the rDivide issue was a real mistake. I made an rDivide2 function that flips the parameters correctly, and the rDivide2 functions passes the tests as expected. This was discussed with Dr. Bowring, and I was surprised to see that I had identified a real error in the code.

Then, just after implementing this, I identified another error. Since I am now serializing all of the parameters needed in a new matrix, I started looking at some of the functions I had not looked at before. One of the first ones I wanted to look at was the linspace function, and I found that there are a couple of issues with it. Mainly, it does not properly compute the linspace whenever there are 1 or 0 total points. I noticed this while generating edge cases in MATLAB.

Since I had already been cleared to fix rDivide, I created a linspace2 function that fixes this by first checking if the "points" parameter is either 0 or 1, and calculating the result accordingly.

Afterwards, I fixed the linspace test to use linspace2, and the function worked properly to high number of sigfigs.

I'm looking forward to next week and potentially finding more bugs.
