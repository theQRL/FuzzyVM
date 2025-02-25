# FuzzyVM

A framework to fuzz Zond Virtual Machine implementations.
FuzzyVM creates state tests that can be used to differential fuzz ZVM implementations against each other.
It only focus on the test generation part, the test execution is handled by [goevmlab](https://github.com/holiman/goevmlab).

## Environment
You need to have golang and go-zond installed

## Install instructions

```shell
# Clone the repo to a place of your liking using
git clone git@github.com:theQRL/FuzzyVM.git
# Enter the repo
cd FuzzyVM
# Build the binary
go build
# Create an initial corpus
./FuzzyVM corpus --count 100  
# Run the fuzzer
./FuzzyVM run
```

# Corpus
It makes sense to create an initial corpus in order to improve the efficiency of the fuzzer.
You can generate corpus elements with `./FuzzyVM corpus --count N`, which will generate `N` corpus elements.

You might create corpus that is to big, you can minimize your corpus with `./FuzzyVM minCorpus`.

# Bench 
You can run a benchmark with `./FuzzyVM bench`. 
