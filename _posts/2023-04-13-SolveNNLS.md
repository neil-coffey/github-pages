This week was a skip week as I was unable to fix errors on the key function that I was try to test.

There are odd issues around the SolveNNLS function. Although I was eventually able to figure out from Ian which MATLAB function this was meant to emulate, I ran into problems (like with cholcov) around randomly generating inputs.

For some reason, in 100 inputs of any size per element, a few times (say, 3) in 100 the solver will run out of its default max iterations.

The only way to modify the max iterations would be to significanlty modify the source code, and this would ruin the purpose of trying to recreate the same outputs in Java. 

There is no discernable pattern in the inputs that cause the solver to run out of max iterations, so I have been stuck looking for an algorithm to generate inputs. 

For next week, I think I'll give up the SolveNNLS function and try to go for the SplineBasisModel function.
