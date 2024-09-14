# This repo contains a bug

## Error:
''''
error: Invalid order of type declarations for serialization.
error: could not compile `groth16_example_bn254` due to previous error
''''

## Specifics:
The error happens when the function ''''multi_pairing_check_bn254_3P_2F_with_extra_miller_loop_result'''' is compiled during ''''scarb build'''' when the project package is inside of a Scarb workplace. Commenting out this function compiles the package properly.

## Notes:
The verifier package is generated from garaga gen, specifically version "v0.13.2.3", using the bn254 verification key in the /hydra/garaga/starknet/groth16_contract_generator/examples directory. 