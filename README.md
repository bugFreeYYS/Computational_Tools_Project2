# Computational_Tools_Project2

# Oct 30 (yuesong)
implement hyperloglog function and its dependencies.

problem:
1. mmh3 is not compatible with MacOS Mojave. I am using pymmh3 instend which is implemented in python only.
2. hash value can be negative, not sure how to deal with negativity. Remove or keep it.
3. seems the index j is never below 10. Result is tested on 20000 values.
4. harmonic mean is not defined for 0.
5. exception handling --> upper part only consists of 0s --> current implementation return positional index to be 0

# 2 Nov (yuesong)
implement reservoir sampling given that domain and ip are given at run time instead of compile time.

problem:
need some testing on accuracy cos seems that i do not get multiple ips on the same domain. (up to 1 * 10^6 streaming data)