# SQRL-Client-Crypto-Diagram
Reference: https://www.grc.com/sqrl/SQRL_Cryptography.pdf

## How to edit
The diagram source can be edited using the online tool at https://www.draw.io/. If a local installation is preferred, an Electron-based desktop version is available at https://github.com/jgraph/drawio-desktop/releases.

## SqrlVect.exe
This is a "Test Vector" program for Windows which applies SQRL crypto, encoding, and decoding functions to input data specified by the user.  Run it from a Windows Command Prompt.
The first time you run SqrlVect.exe it creates SqrlData.txt containing examples of all the input data and functions handled by the program.
It processes SqrlData.txt and outputs the results to the console and to SqrlVect.txt.

For example, to calculate the password-based key for the Rescue Code using EnScrypt, enter the Rescue code, Salt, and Number of Iterations, RC=, SaltRC=, IterRC=, and specify the Rescue Code Based Key function RCBK()

SqrlData.txt contents:

	RC=0123-4567-8901-2345-6789-0123  
	SaltRC=23 45 67 89 ab cd ef 01 23 45 67 89 ab cd ef 01  
	IterRC=16  
	RCBK()

SqrlVect.txt result:
	
	RC=  
	0123-4567-8901-2345-6789-0123  

	SaltRC=  
	23 45 67 89 ab cd ef 01 23 45 67 89 ab cd ef 01  

	IterRC=  
	16  

	RCBK() : EnScrypt(RC, SaltRC, IterRC)  
	71 ec 35 bb d1 25 ef 87 d8 78 5b b6 e8 8e 7b c6 81 8c 12 a8 69 17 a0 22 3a e7 b8 f7 78 bc 8b 8a  
