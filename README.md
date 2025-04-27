# AES_Implementation

In 2001, the National Institute of Standards and Technology (NIST) published Advanced Encryption Standard (	AES). It was created with the intention to replace DES. AES is a symmetric block cipher with a complex structure. AES is a symmetric block cipher with a complex structure, designed to provide a more secure and efficient alternative to DES in modern cryptographic applications. 

AES (Advanced Encryption Standard) is a symmetric block cipher that encrypts 128-bit blocks of data using a 128-bit key. It operates in rounds, and AES-128 has 10 rounds of transformation.
Each round consists of:
SubBytes – Byte substitution using an S-box.
ShiftRows – Row-wise permutation.
MixColumns – Column transformation (except in the last round).
AddRoundKey – XOR with a round key.

The provided Python code implements the fundamental components of the Advanced Encryption Standard (AES) algorithm. It defines the substitution box (S-box) and its inverse (inverse S-box) for the SubBytes and InvSubBytes transformations, along with the round constants (r_con) utilized during the key expansion process. Utility functions such as bytes_to_matrix and matrix_to_bytes are included to facilitate the conversion between byte arrays and 4×4 matrices, which is essential for AES operations. 
Core cryptographic transformations are implemented: add_round_key executes a bitwise XOR between the state and the round key; sub_bytes and inv_sub_bytes perform byte substitution using the respective S-boxes; and shift_rows and inv_shift_rows introduce diffusion by cyclically shifting matrix rows. 
The mix_single_column and mix_columns functions execute the MixColumns transformation to further enhance diffusion, while inv_mix_columns implements its inverse by computing intermediate field operations. 
The xtime function provides multiplication by 2 in the Galois Field GF(2^8), a critical operation within MixColumns. Furthermore, the key_expansion function generates the necessary round keys by expanding the initial cipher key through a combination of byte substitution, word rotation, and XOR with the round constants. 

Collectively, this code establishes the core building blocks required for the encryption and decryption processes in AES.
