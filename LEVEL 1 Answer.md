Parallel and Distributed Computing Final Exam

1. Differentiate between SIMD and MIMD? Explain.

Answer:
SMID - SIMD requires small or less memory and is a type of parallel processing in Flynn's taxonomy. SIMD can be internal (part of the hardware design) and
it can be directly accessible through an instruction set architecture (ISA), but it should not be confused with an ISA.
SIMD describes computers with multiple processing elements that perform the same operation on multiple data points simultaneously.

MIMD - While it requires more or large memory and is a technique employed to achieve parallelism. Machines using MIMD have a number of processors that function
asynchronously and independently. At any time, different processors may be executing different instructions on different pieces of data.

2. What are the performance metrics of parallel systems? Explain each. 

Answer:
Execution time - execution time of a parallel program as the time that elapses from when the first processor starts executing
on the problem to when the last processor completes execution.

Total parallel overhead - Parallel execution entails a cost in terms of the processing overhead necessary to break up a task into pieces,
manage the execution of each of those pieces, and combine the results when the execution is complete.

Speedup - achieved by a parallel algorithm is defined as the ratio of the time required by the best sequential algorithm to solve a problem and also speedup
is a number that measures the relative performance of two systems processing the same problem.

Efficiency - measure of the efficiency of the parallel processor to execute a given parallel algorithm. Any degradation in performance
due to parallelization overhead will result in. being less than one.


4. Explain what pipelining is.

Answer:
What is pipelining explain it?
In computers, a pipeline is the continuous and somewhat overlapped movement of instruction to the processor or in the arithmetic steps taken by the
processor to perform an instruction. Pipelining is the use of a pipeline.
