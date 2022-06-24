This is the source code used to verify some of the security properties of the PSM protocol.

The folder contains the ProVerif code and the executable for ProVerif.

- pprst.pv 
The code is meant to verify the secrecy of the cell identifier a and b from the adversary. 
Moreover, we verify if the attacker is able to brute-force/guess the identifier a and b. 
We verify with ProVerif if the adversary is able to retrieve the value rA (the nonce).


To run the scripts:
- compress the archive
- go to ./ProVerif/
- run our protocol by executing the command:
```properties
 ./proverif.exe pprst.pv 
```  


