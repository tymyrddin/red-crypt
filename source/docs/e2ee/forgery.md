# Forgery attack

This attack can be mounted by an E2EE adversary, able to bypass the client-to-server transport encryption. 

1. Intercept a packet `D` sent by a group member by sniffing traffic between the group member and the service server.
2. Derive salt from `D` and derive `Key` and `Initialisation Vector` from a group key and a public key.
3. Decrypt with `Key` and `Initialisation Vector` and modify a message `M` of the group member.
4. Re-encrypt the modified message `M'` with `Key` and `Initialisation Vector` to generate a new ciphertext `C'` and tag `T'`.
5. Broadcast `D'` including `C'`,`T'` and associated data to all group members except the targeted group member and 
send the original `D` to the targeted member via the service server.


