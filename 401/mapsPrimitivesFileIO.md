

## READ 3
As we all know, there are two systems for Java data types. The First one is **primitive** such as int, byte, short, long, float, double, boolean, and char and it is located in the stack.
on the other hand, some **reference** types must be used in some cases. which are Array, Boolean, Integer ... notice that all of it starts with upper case and it is located in the heap.
autoboxing is when we want to convert between the two data type systems: **primitive**---> **reference**.
 it may differ from a virtual machine to another but the primitive types have some effect on memory for sure:
boolean – 1 bit
byte – 8 bits
short, char – 16 bits
int, float – 32 bits
long, double – 64 bits
We cannot forget the fact that the reference types are objects and it takes much more size than the primitive for it takes :
Boolean – 128 bits
Byte – 128 bits
Short, Character – 128 bits
Integer, Float – 128 bits
Long, Double – 192 bits
It differs from one case to another, but we can say that the single-element arrays of primitive types take more space in memory.
And when it comes to time, reference types take more time to perform the work.
//////////////////////

### Errors and Exceptions: 

Exception in java is the same as errors in any other programming language, so basically, it is the way that Java tells developers that there is something wrong in the code, it also gives us a description of the error so we can handle it. 
here are the three kinds of exceptions:
 checked exception: this happens during compiling the program.
error: when the problem is in the application itself.
 runtime exception: such as bugs,  logic errors, mismatch anything in the code.
to handle these errors, we have several ways, but the best is the (try and catch) way. we use this way in different programming languages such as javascript and java. what it does is to type the code we want to run in the try, if there is any condition that stops it from running, it will go to the catch which is the way to catch errors.

Scanner objects are handy for breaking structured input into tokens and translating each token according to its data type. it will separate between in spaces by default.






