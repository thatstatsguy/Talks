source: https://www.youtube.com/watch?v=blCOHdv30fA

## Compiled code 
- text instructions converted into assembly like representation

## Interpretted code 
- code goes into a processor where it steps through code one line at a time in order to do execution.
- no expectation it will produce an artifact like a dll, it just does the work.


# How does this relate to F#?
- start into a .fs file in F#

## CIL and CLE
- F# can compile the files into a dll or exe 
    - Common Intermediate Language (CIL) is the content of this file
    - CIL is a state machine
- Common Language Runtime does a JIT compile in order to convert the content of the dll into assembly for a x86 runtime or something similar.

## From the produced artifact to the CPU
- assembly goes to memory and then on to CPU
- code within the CPU
    - different cahes L1, L2, L3
    - L1 cache is futher broken down into L1 Data and L1 Instruction cache.
    - Code within the L1 cache is broken down further into something called micro-ops which is one the lowest forms of instructions.
- after it goes into the CPU, the output is compliant with the instruction set agreement (ISA)
    - this is a data contract between the CPU and cache.
    - this contract process can be thought of as a interpretter (kind of related to the the whole compiled vs interpretted discussion at the top)

## JIT
- aim with JIT (one of them) is to get the program running asap
- fastest IL to x86 or similar possible
- does some optimisation on your code by looking at "hot spots" of a program and optimising it as fast as possible.
- This is why benchmarking with something like Benchmarking.net is important. The JIT is going to make things faster the more you run things.

## Which is faster in terms of F#?
- side note, have a look at K programming language

