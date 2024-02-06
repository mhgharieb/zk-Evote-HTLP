# 63-bit Implementation

This is a toy implementation that uses a 63-bit integer for ($N$) to assess the functionality of the protocol and its proposed extensions. The e-voting models include `YES-NO`, `multi-approval`, and `multi-score`.

## E-voting Model Parameters:

- `YES-NO`: `NUMBER_of_VOTERS`
- `multi-approval`: `NUMBER_of_VOTERS`, `NUMBER_of_CANDIDATES`, `NUMBER_of_APPROVAL`
- `multi-score`: `NUMBER_of_VOTERS`, `NUMBER_of_CANDIDATES`, `MAX_SCORE`

## Getting Started:

- Change the directory to one of the `YES-NO`, `multi-approval`, or `multi-score` folders.
<!-- - Run `npm i` to install dependencies -->
- Change the directory to the `build` folder (`cd build`).
- Run one of the following commands to install dependencies and build the zkSNARK artifacts:

    - For `YES-NO`: `./build.sh -n [NUMBER_of_VOTERS]`
    - For `multi-approval`: `./build.sh -n [NUMBER_of_VOTERS] -m [NUMBER_of_CANDIDATES] -a [NUMBER_of_APPROVAL]`
    - For `multi-score`: `./build.sh -n [NUMBER_of_VOTERS] -m [NUMBER_of_CANDIDATES] -s [MAX_SCORE]`

    For example, `./build.sh -n 5` for $5$ voters.
    
- Run `npm run test` to test a full scenario and get the gas cost of each transaction.

# Notes:

- You may need to update the variable `powersOfTau` in `build/build.sh` based on the number of constraints generated by the circuits.
- Find the suitable `powerOfTau` in [snarkjs GitHub](https://github.com/iden3/snarkjs#7-prepare-phase-2).