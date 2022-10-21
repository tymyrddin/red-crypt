# Decrypt the message via recipient

## Attack tree

```text
1 Chosen ciphertext attack on symmetric key (OR)
2 Chosen ciphertext attack on public key (OR)
3 Send the original message to the recipient (OR)
4 Monitor outgoing mail of recipient (OR)
5 Spoof Reply-To: or From: field of original message (OR)
6 Read message after it has been decrypted by recipient.
    6.1 Copy message off user's hard drive or virtual memory (OR)
    6.2 Copy message off backup (OR)
    6.3 Monitor network traffic (OR)
    6.4 Use electromagnetic snooping techniques to read message as it is displayed on the screen (OR)
    6.5 Recover message from printout
```
