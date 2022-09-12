This is the source code used to verify some of the security properties of the PPTM protocol.

The folder contains the ProVerif code and the executable for ProVerif.

- pptm.pv 
The code is meant to verify the secrecy of the capsule identifier dA1 and dB1k from the adversary. 
Moreover, we verify if the attacker is able to brute-force/guess the identifiers dA1 and dB1k.
We verify with ProVerif the strong secrecy, which shows that the adversary cannot distinguish between different secrets.

To run the scripts:
- uncompress the archive
- go to ./ProVerif/
- run our protocol by executing the command:
```properties
 ./proverif.exe pptm.pv 
```  


