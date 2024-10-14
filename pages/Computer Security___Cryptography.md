- ![L06_Crypto_Intro.pdf](../assets/L06_Crypto_Intro_1696410886462_0.pdf)
	- DONE Chapters: 8.1.1-8.1.3
- ![L07_Symmetric_Encryption.pdf](../assets/L07_Symmetric_Encryption_1696410843484_0.pdf)
	- TODO Chapters: 8.1.4, 8.1.6, 8.1.7, 8.5.1
- ![L08_Hashes_And_MACs.pdf](../assets/L08_Hashes_And_MACs_1697630138938_0.pdf)
	- DONE Chapters: 8.3
- ![L09_Asymmentric_Encryption.pdf](../assets/L09_Asymmentric_Encryption_1697630202761_0.pdf)
	- TODO Chapters : 8.2, 8.5.2
- ![L10_Digital_Signatures.pdf](../assets/L10_Digital_Signatures_1697630307420_0.pdf)
	- TODO Chapters: 8.4
-
-
- # Introduction to Cryptography
	- *The scientific study of techniques for securing digital info, transactions, and distributed computations*
	- ## Symmetric Cryptography
	  collapsed:: true
		- ### Goals
			- For Secure communication across Internet
			- Secure Files
		- ### Encryption Schemes
			- Encryption algo $E: K\times M \implies C$
			- Decryption algo $D: K\times C \implies M$
			- \TODO Get slide algo
			- An encryption schemes is good if eve cannot:
				- recover $k$
				- recover plaintext $m$
				- recover any bits of from plaintext $m$
		- ### Kerkhof's Principle
			- The $E$ and $D$ algos are public
			- Security relies entirely on the secrecy of the key $k$
			- *So all security relies on the key*
			- Open designs allows for scrutiny by many people, making it more secure overall
			- Vulnerabilities can be detected, correction can be made
		- ### Adversary capabilities
			- Eve had the algos, but may have access to:
				- Ciphertext attack - some $c_1 ,..., c_n$
				- Known plaintext attack - some $(m_1,c_1),...,(m_n,c_n)$
				- Chosen plaintext attack -
				- Chosen cyphertext attack -
				- Computational Power - unlimited, polynomial, or realistic
					- Only consider realistic
			- Brute force attack
	- ## Substitution Cyphers
	  collapsed:: true
		- ### Caesar cipher
			- Shift letters one left or right
		- ### The *Vigenere Cipher*:
			- Substitution can be applied to whole blocks of letters, not just pairs.
			- Shifts first letter by $k_1$, second by $k_2$, etc until $k_m$
				- e.g. $k[ ]$ = $"MELON"$
				- so $k_1$ shifts first block of letters by 13 as its the 13th letter of alphabet
			- ((652fd171-723f-4247-8943-07aa5ab95768))
			- Bruteforce infeasable, 26! combos
			- Can be broken using frequency analysis (very clever)
				- Letters frequency:
				  ((652fd25e-8665-4352-afd9-2f4b94d44e47))
				- Digrams/trigrams frequency (an |the > and > ing)
				- Expected words
		- ### One Time Pad (OTP)
			- 2 critical differences:
				- For length $m$ of block of keys and length $n$ of plaintext $m=n$
				  logseq.order-list-type:: number
				- Each shift amount must be *completely* random
				  logseq.order-list-type:: number
			- No statistical analysis can be done
			- *unless* pads are reused
			- Are impractical
		- ### Binary OTP
			- We view plaintext as a binary string
			- Pad P is random binary string of the same length
			- We us $C = M \oplus P$
			- As XOR is associative, pad P both encrypts and decrypts
				- so $M = C \oplus P$
		- ### Perfect Secrecy
			- ((652ff214-d32f-44d6-b056-8a0e1c169efc))
		- ### Limitations of OTP
			- Key length
			- True Randomness is impossible
			- 2-time pad attacks
			  ((652ff24a-341d-49f2-98db-e7701a6f6205))
			- Perfect secrecy does not mean completely invulnerable
				- 2-time pads
				- Malleability
-
- # Symmetric Encryption
	- ## Pseudo-Random Number Generators (PRNG)
		- ### Linear Congruential Generator
			- Used by java
			- Start with random number
			- $x_{i+1} = (ax_i + b)$ $mod$ $n$
			- Drawbacks:
				- Easy to predict $x_{i+1}$ once youve seen 3 consecutive numbers
				- Its period, will start repeating sequence after a while
		- ### More secure PRNGs
			- Use ((652ff4c5-278f-4b84-b20e-321d7a5b630d))
			- Period is $2^n$
			- However, should still any use any key once
		- ### The Advanced Encryption Standard (AES)
			- Block Cypher that works on 128 bits
			- TODO AES and RSA
-
- # Cryptographic Hashs and MACs
  collapsed:: true
	- ## Properties and Applications
		- ### Collision Resistance
			- TODO why is collision bad?
			- Hash function $H$
			- *Weak* CR
				- Avoid collisions with a specific message
				- For a given message M it is difficult to find another message M' such that 
				  $$H(M)=H(M')$$
			- *Strong* CR
				- Avoid collision in general
				- For 2 distinct messages $M_1$ and $M_2$ is is dificult to compute
				  $$H(M_1)=H(M_2)$$
		- ### Merkle-Damagard Construction
			- Uses *Cryptographic Compression Function*  
			  $$C(X,Y)$$
			- Given message $M$, we divide it into multiple blocks $M_1,M_2,...M_k$
				- If needed, add padding to the last block
			- Using *initilization vector* $v$, we calculate vector $d_1$ with 
			  $$d_1=C(M_1,v)$$
			- Followed by $d_2$
			  $$d_2=C(M_1,d_1)$$
			- Reapeat untill the end
			- ((652ffb7e-0e5f-4cf1-9be5-36d08da9e0d4))
		- ### Practical Hash Functions
			- Currently recommended are the *Secure Hashing Algorithms* SHA-256 and SHA-512
			- They work like the M-D construction
	- ## Birthday Attacks
		- The main way CHFs are attacked is by compromising compression resistanc
		- ((652ffcc9-3842-482a-94e8-62694f366e10))
		- Eve doesn't try to number of messages $2^b$, just $2^{b/2}$
		- Thus for a 256 bit hash function has half the security, 128 bit
-
- # Asymmetric Encryption
- ## RSA Cryptosystem
	- ### Setup
		- Bob (receiver) generates two large random prime numbers $p$ and $q$ and setting $n=pq$
		  logseq.order-list-type:: number
		- Picks a number $e$ relatively prime to $φ(n)$ and computes private key $d$ where
		  logseq.order-list-type:: number
		  $$d=e^{-1} \; mod \;φ(n)$$
		- Throws away $p,q$ and $φ(n)$
		  logseq.order-list-type:: number
		- Sends public key ($e,n$) to Alice
		  logseq.order-list-type:: number
	- ### Encryption/Decryption
		- Alice can encrypt message $M$ with 
		  logseq.order-list-type:: number
		  $$C=M^e \; mod \; n$$
		- Bob decrypts cypher C with
		  logseq.order-list-type:: number
		  $$M = C^d \; mod \; n$$
	- ### Security of RSA
		- Important to keep p and q secret, so we destroy it
		- The system is tied to the factoring n problem, so far unsolved
		- If $C_1 = C_2$ then $M_1 = M_2$, so some info can be inferred
- ## Elgamal Cryptosystem
	- TODO ((6530042e-6145-4c9c-aef8-7a7afd5a0287))
- ## Key Echange
	- ### Key Exchange Protocols
		- Cryptographic to establishing a shared secret key
		- Doesn't work if key exchange can be disrupted
		- Can still be established if only passive eavesdropping occurs
	- ### Diffie-Hellman (DH) protocol
		- Prime number p is established from generator
		- ((653048e4-b17f-41f8-8b64-96b3769fbba1))
	- ### Man in the middle attack
		- ((6530491a-1bfd-4d7b-8eb6-494a00a9f051))
- ## RSA
	- Oh god maths no pls no make it stop help
	- ((65304980-6083-4cf4-979f-a400b5514d46))
	- ((6530498b-58f7-45a7-9d03-35669899f0b8))
-
- # Digital Signatures