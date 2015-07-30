The client folder must be placed in in the lua/autorun folder in your Just Cause 2 Multiplayer Mod Dedicated Server directory, or wherever your scripts are stored.
The Crypt and CryptVec functions work cross-module by having a consistent cipher between all modules - the function can be used anywhere on the client.
XOR Encryption reverses itself, so encrypting and decrypting a string is done by calling the same function.
For example: Crypt(var) will encrypt the value and then doing Crypt(var) again will decrypt the value.
The Crypt() function must not be used to decrypt vectors, however, it can be used to encrypt vectors.
The CryptVec() function was added to DECRYPT vectors. It must NOT be used to encrypt ANYTHING.
All encryption is automatically stored as variable type string.
You can get an encrypted number back by doing tonumber(Crypt(var)).
This encryption is useless against code-injection(very unlikely) but is far superior to obscurity through math operations.