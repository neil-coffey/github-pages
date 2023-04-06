This week was another skip week. I ran into some issues involving some of the functions that I was trying to add test files for. Unfortunately, I wasn't able to resolve these issues, but they involve 2 problems:

1. Some of the functions in MatLabTest.java have multiple parameters that make serialization more difficult. It would not be efficient to create new serialization functions, so I will try to come up with the most elegant solution.

2. The SplineBasis model generator seems to function differently than MATLAB. This confuses me somewhat and I'll just need to discuss it with Dr. Bowring. 

Otherwise, there are odd and pervasive errors that continue to occur, such as how some serializations for kronTest() do not work, while others do. 

Leaving the errors aside, my developments this week include adding the rounding function to the MatLab.java file. This rounding function, provided by Dr. Bowring, uses BigDecimal to perform math and round large numbers properly and precisely. I was able to add this to the previously implemented tests and was able to verify the decimal/rounding point of about 7 functions for the MatLab.java file.
