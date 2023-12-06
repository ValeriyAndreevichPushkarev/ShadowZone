# Shadow Zones
Shadow Zones Computations

The main idea is to use positional encoding to preform a calculations without any active elements(except NOT element).

### For example here is function with 2 digits(1): ###

A B   Result

01 **0**1  **0**

01 10  1

10 **0**1  **0**

10 10  1

Result = First Digit of B


### Lets take another example (2): ###

A B   Result

**0**1 **0**1  **0**

01 10  1

10 01  1

10 10  1

Result = "Shadow" from first part of A (01) and "shadow" from first part of B (01).


### Lets suppose another example (3): ###
A B   Result

**0**1 **0**1  **1** - inversion

01 10  0

10 01  0

10 10  0

Simply invert previous result



### Example of AND (4): ###

A B   Result

01 01  0

01 10  0

10 01  0

1**0** 1**0**  **1** - inversion

### As you can see here we get **OR** (2) and **AND** (4) operations so we can compute anything :).
In most complicated cases we can simply add an invertor.

Simply invert result from two zero's in a digit notation.


Its easy to invert the results - with the help of quasi-stationary light\electromagnetic elements.

That simple trick allows to build supereffective computations based on light **or electromagnetic waves** (much more effective than anything).

Thats **works only with positional (one-hot) encoding** (where **you always have a zeros in a digit notation**).

And, 50 mw laser can provide enought light to compute almost anything (optics, km's of optics). 

No coherence, no headache with all other.

**Use less logical elements that your bitness. Always keep in mind activity factor.**


## TODO: ##

Add results in one-hot encoding
