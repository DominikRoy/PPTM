# PPTM ProVerif

This is the source code used to verify some of the security properties of the PPTM protocol.

The folder contains the ProVerif code and the executable for ProVerif.

- pptm.pv 
The code is meant to verify the secrecy of the capsule identifier dA1 and dB1k from the adversary. 
Moreover, we verify if the attacker is able to brute-force/guess the identifiers dA1 and dB1k.
We verify with ProVerif the strong secrecy, which shows that the adversary cannot distinguish between different secrets.

### Instructions for Windows:
- download the ProVerif binary for [Windows](https://bblanche.gitlabpages.inria.fr/proverif/proverifbin2.04.tar.gz)
- clone the git repository or uncompress the archive
- go to ./ProVerif/
- run our protocol by executing the command for Windows:
```properties
 ./proverif.exe pptm.pv 
```  

### Instructions for Linux (Ubuntu 20.04):
- make sure the packages: [ocaml](https://packages.ubuntu.com/search?suite=default&section=all&arch=any&keywords=ocaml&searchon=names), [ocaml-compiler-libs](https://packages.ubuntu.com/search?keywords=ocaml-compiler-libs) and [LablGTK2](https://packages.ubuntu.com/search?suite=default&section=all&arch=any&keywords=LablGTK2&searchon=names) are installed:

```
sudo apt-get install -y ocaml ocaml-compiler-libs ocaml-findlib liblablgtk2-ocaml-dev 
```
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
- clone the git repository into the current folder where the command above was executed
- run our protocol by executing the command for Linux:
```properties
 ./proverif /PPTM/ProVerif/pptm.pv
```
### Instructions for Docker:
- make sure [docker](https://docs.docker.com/engine/install/) is installed
- clone the git repository of PPTM
- the repository contains a `Dockerfile`, which builds the docker image. Therefore, execute following command to create the docker image:
```
sudo docker build -t proverif .                                                                              
```
- after building the docker image execute following command to execute pptm proverif code:
```
sudo docker run -it proverif:latest ./proverif2.04/proverif /home/proverif/proverif2.04/PPTM/ProVerif/pptm.pv
```
