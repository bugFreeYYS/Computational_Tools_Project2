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

# 4 Nov (yuesong)

1. HyperLogLog bugs are fixed. should be up and running.
2. HyperLogLog are updated to match wiki implementation which avoid many problems occurred previously.
3. HyperLogLog at scale is implemented
4. Countmin at scale is implemented
5. Reservoir sampling is replaced by Countmin at scale for qn 3. seems reservoir sampling is not appropriate. still keep the implementation for further uses.

# 4 Nov (ziyue)
1. readablity improvements including small tweaks to the HyperLogLog & CountMean function
2. HyperLogLog: list index out of range error starts to appear for stream sizes >= 15692
3. Will complete analysis tmr

# 4 Nov evening (ziyue)
1. implement qn 4 and 5:
    - How many unique IPs are there for the domains  𝑑1,𝑑2,… ?
    - How many times was IP X seen on domains  𝑑1,𝑑2,… ?
    
# 4 Nov(qing)
implement the accuracy of countMin function
will check with ziyue tmr evening 

# 6 Nov (ziyue)
1. add code cell to install pymmh3 and scipy (feedback from the last assignment)
2. merge countMin() and getResult() into one function (q2 and q4)
3. q5 topX most frequent IP implemented.

# 7 Nov (ziyue)
1. fix q5, now the topX algo is able to dynamically adjust its size to resolve ties. yay :)
2. implement exact counts dictionary {domain1 : {IP1 : occurrences1, IP2 : occurrences2, ...}, domain2: {IP1 : occurrences1, ...}, ...}

# 8th Nov (yuesong)
1. def getResult(stream, IP_X, Domain_Y, w=16, d=5), if we have stream, X and Y at the beginning, we should not build dictionary. we just filter Y and count distinct X. So i guess, ....
2. topX seems need to store IPs into a dictionary. I am not sure if streaming allows it. I have implemented a different version.

# 8th Nov (yuesong)
1. section 1 and 2 cleaned. done.
2. analysis of accuracy: seems none of the estimates are accurate..

