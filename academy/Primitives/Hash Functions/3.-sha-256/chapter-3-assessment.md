# Chapter 3 - Assessment



1. What is the bit length of a SHA-256 output hash, and how is it usually expressed?

a) 160bits, base10

**b) 256bits, base16**

c) 512bits, base2

d) 256bits, base8

&#x20;

2\. What hash function(s) is used to generate a transaction identifier (TXID) & Block ID?

a) SHA-512

b) RIPEMD-160

c) HASH-160

**d) HASH-256**

&#x20;

3\. Use the [hash calculator](https://bitcoinsv.academy/hash-calculator) to find the message digests for the given input strings using the specified hash functions:

| **Input Message**                                                                                          | **Hash Function** | **Message Digest**                                                   |
| ---------------------------------------------------------------------------------------------------------- | ----------------- | -------------------------------------------------------------------- |
| <p> </p><p><code>1hash functions map an arbitrary length input to a fixed length output</code></p><p> </p> | SHA-256           | **43413cd5705ae60f89856a54dede636d8f3a7e781461afc86ac3fe5d86b6f604** |
| <p> </p><p><code>1hash functions map an arbitrary length input to a fixed length output</code></p><p> </p> | SHA-256(SHA-256)  | **6f108ad8346c21d32841937e5e6b0074f223c75b9695c02d9d6428071066d5b9** |
| <p><code>1hash functions map an arbitrary length input to a fixed length output</code></p><p> </p>         | HASH-256          | **6f108ad8346c21d32841937e5e6b0074f223c75b9695c02d9d6428071066d5b9** |

&#x20;

4\. Use the [hash calculator](https://bitcoinsv.academy/hash-calculator) to calculate the TXID for the following transaction

| **Serialised TX in HEX**                                                                                                                                                                                                                                                                                                                                                                         | **TXID in Little Endian**                                            | **TXID in Big Endian**                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `010000000167e7105b52e8534596af29dba949921cffe3dbaa555b8ed96121346c6755adae000000006a47304402206e4db9dee8449b861e5fdc00ba3bdb80fba8cd52c75489376c54bd65d26262650220453569438e6bc6f957b1f7ff6fff4af2e42edaae1ac885382373d42fa569b17c41210267d2d1f8b3affffa10b68b2756ba7f6f4efafcadbecd145181016178d00b379bffffffff019c276bee000000001976a914accd105073775756cc04962bc1e4893694f50c5588ac00000000` | **33e189f51be6bf7434f893f3a53513f664f25b00d15d96810bd27d3bbe307c35** | **357c30be3b7dd20b81965dd1005bf264f61335a5f393f83474bfe61bf589e133** |

&#x20;

5\. Divide the following transaction up into its constituent elements:

| `01000000011e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b000000006b483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003ffffffff0200943577000000001976a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac8f933577000000001976a914e33649e455368d536f6003b2908b6299df5fe8bf88ac00000000` |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| **Version** | **Input Count** | **Input List**                                                                                                                                                                                                                                                                                             | **Output Count** | **Output List**                                                                                                                            | **nLocktime** |
| ----------- | --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------- |
| `01000000`  | `01`            | `1e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b000000006b483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003ffffffff` | `02`             | `00943577000000001976a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac8f933577000000001976a914e33649e455368d536f6003b2908b6299df5fe8bf88ac` | `00000000`    |

6\. Using the transaction from the previous question, divide the input UTXO into its constituent elements:

| `01000000011e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b000000006b483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003ffffffff0200943577000000001976a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac8f933577000000001976a914e33649e455368d536f6003b2908b6299df5fe8bf88ac00000000` |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| **Previous TX Hash**                                               | **Previous Output Index** | **Input Script Length** | **Input Script**                                                                                                                                                                                                         | **Sequence Number (nSequence)** |
| ------------------------------------------------------------------ | ------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------- |
| `1e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b` | `00000000`                | `6b`                    | `483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003` | `ffffffff`                      |

&#x20;

7\. Using the transaction from the previous question, divide the output UTXO(s) into its constituent elements:

| `01000000011e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b000000006b483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003ffffffff0200943577000000001976a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac8f933577000000001976a914e33649e455368d536f6003b2908b6299df5fe8bf88ac00000000` |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| `01000000011e4bf9dc623d942fee4113e077f67204419cb6f841d98ebf250b698cbea8912b000000006b483045022100a7ce3b1d8cc852e625e5da3159131ba7ba071c7a93684f1d3b8d08b6dbc08e82022041ac850772b5877cc8b724f6a7a92709a65a17a52f78419b67304f2481526b79412102e8a1ab43a501a2ab84a14c5ef1a65c15add65f3ec8230e3fb63644a44ac71003ffffffff0200943577000000001976a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac8f933577000000001976a914e33649e455368d536f6003b2908b6299df5fe8bf88ac00000000` |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| **Output Count** | **Value**  | **Output Script Length** | **Output Script**                                    | **Locktime** |
| ---------------- | ---------- | ------------------------ | ---------------------------------------------------- | ------------ |
| `02`             | `00943577` | `0000000019`             | `76a914aa5604bae61cd60690dd9dec5efbb841668cb19288ac` |              |
|                  | `8f933577` | `0000000019`             | `76a914e33649e455368d536f6003b2908b6299df5fe8bf88ac` | `00000000`   |

\
