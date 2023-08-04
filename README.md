# ZK SNARK Assessment Circuit

This repository contains a circuit written in Pragma Circom  to check if `q` is 0 when the input of `a` is 0 and `b` is 1. The circuit includes custom templates for AND, NOT, and OR gates, which are then used to create the main assessment circuit.

## Description

The assessment circuit consists of three basic gates: AND, NOT, and OR.

1. AND Gate:
   - Inputs: `a`, `b`
   - Output: `out`
   - Description: The output `out` will be 1 if and only if both inputs `a` and `b` are 1.

2. NOT Gate:
   - Input: `in`
   - Output: `out`
   - Description: The output `out` will be the logical negation of the input `in`.

3. OR Gate:
   - Inputs: `a`, `b`
   - Output: `out`
   - Description: The output `out` will be 1 if either input `a` or `b` is 1, or both.

The assessment circuit is constructed using these gates to check the specified condition (`q = 0` when `a = 0` and `b = 1`).

## How to Use

1. Clone this repository to your local machine.

2. Install Pragma Circom 2.0.0 following the instructions mentioned in the official repository: [https://github.com/iden3/circom](https://github.com/iden3/circom)

3. Open a terminal and navigate to the directory containing the cloned repository.

4. Compile the circuit using Pragma Circom:
   ```
   circom circuit.circom -o circuit.json
   ```

5. Use `snarks` to generate the proving key, verification key, and the initial witness:
   ```
   snarks setup
   ```


## Sample Input Format (input.json)

```json
{
  "a": 0,
  "b": 1
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
