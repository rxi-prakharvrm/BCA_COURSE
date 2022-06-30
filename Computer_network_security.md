# Computer Network Security Notes

## <span style="color:gold;"> Access Control </span>

---

1. Access Control is a privacy feature that enables authorised users to access the system, in contrast it disallows the unauthorised persons.

2. _For example, when a user wants to access the **ATM** Machine, he enters the pin and then the system check for the user authentication if the user is authenticated, machine allows him to withdraw the money else it doesn't allow the user to do so._

## <span style="color:gold;"> Data Confidentiality </span>

---

1. Data Confidentiality is roughly equivalent to _data privacy_.

2. Data Confidentiality is a measure undertaken to ensure that the data doesn't go into the wrong hands.

## <span style="color:gold;"> Substitution Cipher </span>

---

In substitution cipher, each letter of the plain text is replaced by another letter, number or symbol i.e.

1. Cipher is a substitution cipher in which each letter in the alphabet is replaced or substituted by another alphabet that is three position forward.

   a -> d, b -> e and so on.

   **Formula:**

   - C = E(P) = (P+3) mod 26
   - P = D(C) = (C-3) mod 26

2. This cipher is also called as **shift transformation**.
3. This is very easy to break.

## <span style="color:gold;"> Transposition Cipher </span>

---

1. Transposition cipher is different from substitution cipher as it encrypt and decrypt data by performing some sort of permutations.

2. In transposition cipher, the letters of the plain text are just transposed to create different permutation of cipher text.

3. For Example:

| Plain Text                           | Cipher Text                   |
| ------------------------------------ | ----------------------------- |
|                                      | `T I I T E N Y A T C M O T O` |
|                                      | `H S S H O L W Y O O E U N W` |
| THIS IS THE ONLY WAY TO COME OUT NOW | tiitenyatcmotohssholwyooeunw  |

## <span style="color:gold;"> Block Cipher & Stream Cipher </span>

---

| <span style="color:gold;"> Block Cipher </span>                                                  | <span style="color:gold;"> Stream Cipher </span>                                                    |
| ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| 1. Block Cipher converts the plain text into cipher text by taking plain text's block at a time. | 1. Stream Cipher converts the plain text into cipher text by taking 1 byte of plain text at a time. |
| 2. Block Cipher uses either 64 bits or more than 64 bits.                                        | 2. While stream cipher uses 8 bits.                                                                 |
| 3. The complexity of block cipher is simple.                                                     | 3. While stream cipher is more complex.                                                             |
| 4. Block Cipher uses confusion as well as diffusion.                                             | 4. Stream cipher only uses confusion.                                                               |
| 5. In block cipher, reverse encrypted text is hard.                                              | 5. While in stream cipher, reverse encrypted text is easy.                                          |
| 6. Slow as compared to stream cipher.                                                            | 6. While stream cipher is fast in comparison to block cipher.                                       |

<!-- ## <span style="color:gold;"> Playfair Cipher </span>

---

1. The Playfair Cipher is manual symmetric encryption cipher.

2. The playfair Cipher encrypts pairs of letters(diagraphs), instead of single letters as the case with simpler substitution ciphers such as the ceaser cipher

3. Frequency Analysis is still possible on the Playfair cipher however it would be against 600 possible paris of letters instead of 26 different possible letters.

4. Playfair cipher is much more secure that the older substitution ciphers.

> ### Steps to create a Playfair Cipher

- Let's say we want to use the phrase **"Hello World"** as our key.
- The first characters (going left to right) in the table will be the phrase with duplicate letters removed.
- The rest of the table will filled with the remaining letters of the alphabet, in order.
- Our key table world look like this:
- |     |     |     |     |     |
  | --- | --- | --- | --- | --- |
  | H   | E   | L   | O   | W   |
  | R   | D   | A   | B   | C   |
  | F   | G   | I/J | K   | M   |
  | N   | P   | Q   | S   | T   |
  | U   | V   | X   | Y   | Z   | -->

## <span style="color:gold;"> Symmetric and Asymmetric Cryptography</span>

---

| Symmetric                                                                       | Asymmetric                                                                                            |
| ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 1. It only requires a single key for both encryption and decryption.            | 1. It requires two keys, a public key and a private key, one to encrypt and the other one to decrypt. |
| 2. The size of cipher text is the same or smaller than the original plain text. | 2. The size of cipher text is the same or larger than the original plain text.                        |
| 3. The encryption process is very fast.                                         | 3. The encryption process is slow.                                                                    |
| 4. It is used when a large amount of data is to be transfered.                  | 4. It is used to transfer small amounts of data.                                                      |
| 5. It only provides confidentiality.                                            | 5. It provides confidentiality, authenticity, and non-repudiation.                                    |
| 6. The length of key used is 128 or 256 bits.                                   | 6. The length of key used is 2048 bits or higher.                                                     |
| 7. Examples: 3DES, AES, DES and RC4                                             | 7. Examples: Diffie Hellman, ECC, EL Gamal, DSA and RSA                                               |

## <span style="color:gold;"> AES VS DES</span>

---

| AES                                                                                       | DES                                                                                                                                                                                                         |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. AES stands for Advanced Encryption Standard.                                           | 1. DES stands for Data Encryption Standard.                                                                                                                                                                 |
| 2. Byte-Oriented.                                                                         | 2. Bit-Oriented                                                                                                                                                                                             |
| 3. Key length can be 128-bits, 192-bits and 256-bits.                                     | 3. The key length is 56-bits in DES.                                                                                                                                                                        |
| 4. Number of rounds depend on the key length: 10(128-bits), 12(192-bits) or 14(256-bits). | 4. DES involves 16 rounds of identical operations.                                                                                                                                                          |
| 5. AES is more secure than the DES cipher and is the de facto world standard.             | 5. DES can be broken easily as it has known vulnerabilities. 3DES(Triple DES) is a variation of DES which is secure than the usual DES as it uses three keys of 56-bits instead of only one key of 56-bits. |
| 6. AES can encrypt 128 bits of plaintext.                                                 | 6. DES can encrypt 64-bits of plaintext.                                                                                                                                                                    |

## <span style="color:gold;">RSA (Rivest Shamir Adleman)</span>

---

It is a popular encryption standard or encryption algorithm. It is widely used for data sent online and relies on a public key to encrypt the data. Those on the receiving end of the data will have their own private key to decode the messages. It's proven to be a secure way to send information between people who may not know each other and want to communicate without compromising their personal or sensitive data.

1. Choose two different large random prime numbers p and q.
2. Calculate **<span style="color:violet">n = pq</span>**
3. Calculate **<span style="color:violet">ϕ(n) = (p-1)\*(q-1)</span>**
4. Choose e (_public key_) such that **<span style="color:violet">1<e<ϕ(n)</span>**
5. e is co-prime to ϕ(n), **<span style="color:violet">gcd(e, ϕ(n)) = 1</span>**
6. Calculate d (_private key_) such that **<span style="color:violet">de ≡ 1 mod ϕ(n)</span>**
7. Public key 'e' and Private key 'd'

## <span style="color:gold;">Internetwork Security</span>

---

1. The security of an internetwork or a local network is called **Internetwork Security**.

2. Internetwork security is implemented to control the confidentiality, integrity, and availability of your information by any means.

![Internetwork_Security_Image](https://img.brainkart.com/imagebk9/pfebZo6.jpg)

## <span style="color:gold;">Three Security Goals</span>

---

1. Confidentiality
2. Integrity
3. Availability

### 1. Confidentiality

The first goal of Network Security is **Confidentiality**. The function of confidentiality is to protect precious business data from unauthorized persons.

### 2. Integrity

The second goal of Network Security is **Integrity**. Integrity aims at maintaining and assuring the accuracy and consistency of data.

### 3. Availability

The third goal of network security is **Availability**. The function of Availability in Network Security is to make sure that the Data, Network Resources or Network Services are continuously available to the legitimate users, whenever they require it.