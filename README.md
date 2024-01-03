# Shadow Zones
Shadow Zones Computations

The main idea is to use positional encoding to preform a calculations without any active elements **with incoherent light or EM wave source**. 
With adding a radiant fluxes (or absense of them).

![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/8b50679b-3953-48f5-a4ea-6b6e47e65969)

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


Its easy to invert the results.

That simple trick allows to build supereffective computations based on light **or electromagnetic waves** (much more effective than anything).

And you can also change light flow (and simply add mirrors on the ends of optical fiber parts that dont conduct light further).

Thats **works only with positional (one-hot) encoding** (where **you always have a zeros in a digit notation**).

And, 50 mw laser can provide enought light to compute almost anything (optics, km's of optics). 

No coherence, no headache with all other.

**Use less logical elements than your bitness. Always keep in mind activity factor.**

## Most intresting moment ##
Wait, we can always change 2 codes between each other (or always "inverse" the second operand without any logical element, just change wiring :) )
Or simply declare two more encodings

OR Upper (ORU)

A B   Result

**0**1 **0**1  **0**0

01 10  10

10 01  10

10 10  10


AND Lower (ANDL)

A B   Result

01 01  01

01 10  01

10 01  01

1**0** 1**0**  0**0**

NAND Lower (NAND-L from ORU)

A B   Result 

00 00  00

00 10  01

10 00  01

10 10  01

OR from ANDL (NOR-L from ANDL)

A B   Result  

01 01  01

01 00  01

00 01  01

00 00  00

OR from NOR-L (NOR-L from ANDL)

A B   Result  

01 01  01

01 00  01

00 01  01

00 00  00

And check how to implement AND and OR operations based in that encodings.

(in progress)

ORU - ORU


AND

A B   Result (NAND-L)

00 00  00

00 10  01

10 00  01

10 10  01

As you can see, we cant simply stay inside Only Low bits or Only High bits encodings.


## The Result ##

So most useful scenario for that computation technique:

![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/8b50679b-3953-48f5-a4ea-6b6e47e65969)

The represented truth table is:

![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/edc6e0fa-3332-4c2a-946f-84b5c8933b11)


Another example - when you can simply detect group of the result (usually the same digit):
![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/623a068d-f521-40d9-8b55-a097d5a9bb3f)



That can be used in **work with matricies** or so (with the base of 4b and branching factors that close to 1000, or even 1M). (Just **encode digit once, and preform thousands of calculations**).
Also we can use em waves that much easier to detect or filter (quazistationary levels of electrons and allowed energy levels).
Also with EM waves is much easy to simply reflect or percolate em waves (compared with the light).

**Modern photodiones have response time about 35 pS (or work on 10 Ghz)**. (https://www.thorlabs.com/thorproduct.cfm?partnumber=FDS015)

With **branching factor of thousands or even millions**, and **near-zero losses in fiberoptics** its absolutely overkill.

Note that its about **3 dB/km signal loss for fiber optics** (or we get only 0.70 of the power of the signal from 1 km line).

Lets make a computations for 15 mW laser (not a diode - diodes much more effective).

**For diode from above with responsibility 0.36 A/W, and branching factor of 100000 for 15 mW laser (!) we have 12 mW/100000 * 0.36 = 40 nA that is 100 more than the dark current (0.5 nA). Notice that this is not a top-notch diode**

Of cause, we always can change diodes to another, more efficient ones.

And **all "Computations" preforms only within a optics**, and only one remaining problem is the branching factor.

And there is a possibility to create efficient invertors (even from LED's and photoionization :)

## Computations only with a Passive elements and a light or em waves ##
Basically you can simple add radian fluxes.

And encode bits with a different radian fluxes (1, 1/(2*n+1) - for functions with 2 arguments, etc).

So you will get different sums of fluxes :).
![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/b2d2fbc7-c39d-44bd-a8b6-ee853cab0a6e)

Principle is simple - we just chage insolations of our "bits".
If we encode our bits with radian fluxes 1 and 1/3 we will get:

![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/abe100de-41b9-4cd8-b437-3f8c15fa0fa1)

The correct radian fluxes for the group 1 is 1 and 0,333.

Another example:
![image](https://github.com/ValeriyAndreevichPushkarev/ShadowZone/assets/130975795/cbecf45f-2076-46dc-bf2b-4c61247a5042)

With that approach we can make absolutely effective computations (on Thz) without any active elements.

Note that its possible to use another basis (not 1b functions, 4b fucntions or even 8b functions can be computed using that technique).

Computations without active evements with uncoherent light or em waves.

Or even use the transistors to "filter EM waves" and detect\inverse them :)

## TODO: ##

Add results in one-hot encoding
