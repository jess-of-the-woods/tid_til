[security](index.md) | [math](../math/index.md)

## Encryption

#### Symmetric
Key works for locking & unlocking. Trouble with symmetric keys is that you can't securely share keys over an unencrypted channel prior to initiating communication.

Algorithm is cheap to use.

### Asymmetric
- public & private keys
- SSH
- HTTPS

**Bob**
- private: spaghetti
- public: ravioli

**Alice**
- private: bananas
- public: apples


### Hashing
- Protects server databases from break in.., being hacked.
- transforms text ( to cyphertext ) by applying  algorithm, one-way process ( 1 way function )
- hard to predict
- bcrypt ( blowfish is publicly available hashing algorithm )
- hashes kinda work like maps, deterministic.. same input & algorithm will always return same output/hash
- on each login, hash is applied

### Review

- HTTPS, ( salt )
