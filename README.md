Download Link: https://assignmentchef.com/product/solved-blockchain-homework-2
<br>
In this lab, you will implement preliminary parts of the ScroogeCoin cryptocurrency. In the next lab, you will act as Scrooge and verify transactions sent to you by users and add them to your blockchain.

<ol>

 <li>Download and install the Java Unlimited Strength Jurisdiction files from</li>

</ol>

http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html. These files remove any restrictions on cryptographic strengths. Read the README file to understand why this step is needed and how to carry out the installation. If you don’t install these files, you will get an “Illegal key size” exception when trying to generate keys.

<ol start="2">

 <li>In this lab and future labs, you must use cryptographically secure random number generation where necessary. Read the following link on generating cryptographically secure random values in Java:</li>

</ol>

https://www.cigital.com/blog/proper-use-of-javas-securerandom/

In your submission, answer the following questions:

<ol>

 <li>Can the Java SHA1PRNG be used securely for cryptographic operations such as generate private/public key pairs?</li>

 <li>What pitfalls do programmers have be aware of when using pseudo-random number generators for cryptographic operations?</li>

 <li>Why should a programmer be concerned about using getInstanceStrong() in certain types of applications?</li>

 <li>In ScroogeCoin, the central authority Scrooge receives transactions from users. Scrooge signs all hash pointers in the ScroogeCoin blockchain. To generate signatures, you will need to generate a private/public key pair on your computer that you can use to digitally sign transactions.</li>

</ol>

Bouncycastle (https://www.bouncycastle.org/) is a popular Java crypto library used in real world crypto systems. The lab includes a lib directory that contains the jars for this library.

Read and thoroughly understand the CryptoReference2.java file which uses crypto primitives like what Bitcoin uses. Try running the CryptoReference2 program on your computer and confirm that it completes successful without throwing exceptions. This program generates ECDSA keys. Read more about this type of cryptographic algorithm at https://en.bitcoin.it/wiki/Elliptic_Curve_Digital_Signature_Algorithm.







<ol start="4">

 <li>Fill in the GenerateScroogeKeyPair.java main method with code that does the following: A. Generates a ECDSA key pair for Scrooge.</li>

 <li>Stores the private key in an encrypted format on disk.</li>

 <li>Store the public key in a separate, unencrypted file.</li>

</ol>

Run the class to generate the key pair for Scrooge. Name the key files as scrooge_sk.pem and scrooge_pk.pem so that it is clear who they belong to. You will use this key pair for the remaining parts of this lab.

In your submission, include your code and the contents of the file containing Scrooge’s public key. Do not submit your secret key. Remember never to give out your secret key and to always encrypt the secret key file when storing it on disk.




<ol start="5">

 <li>Fill in the GenerateDigitalSignature main method with code that does the following:</li>

 <li>Reads Scrooge’s key pair from disk</li>

 <li>Generate Scrooge’s digital signature for the message “Pay 3 bitcoins to Alice”. Do not include the quotations in the message. Capitalization matters.</li>

</ol>

In your submission, include your code and the digital signature in hexadecimal.