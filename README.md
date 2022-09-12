This is the source code used to verify some of the security properties of the PPTM protocol.

The folder contains the ProVerif code and the executable for ProVerif.

- pptm.pv 
The code is meant to verify the secrecy of the capsule identifier dA1 and dB1k from the adversary. 
Moreover, we verify if the attacker is able to brute-force/guess the identifiers dA1 and dB1k.
We verify with ProVerif the strong secrecy, which shows that the adversary cannot distinguish between different secrets.

To run the scripts for Windows:
- download the ProVerif binary for [Windows](https://bblanche.gitlabpages.inria.fr/proverif/proverifbin2.04.tar.gz)
- clone the git repository or uncompress the archive
- go to ./ProVerif/
- run our protocol by executing the command for Windows:
```properties
 ./proverif.exe pptm.pv 
```  

To run the scripts for Linux:
- download the source of ProVerif for [Linux](https://bblanche.gitlabpages.inria.fr/proverif/proverif2.04.tar.gz)
- extract archive:
```properties
 tar -xf proverif2.04.tar
```
- navigate to the folder and build the program:
```properties
 cd proverif2.04
 ./build
```
- run our protocol by executing the command for Linux:
```properties
 ./proverif pptm.pv
```
