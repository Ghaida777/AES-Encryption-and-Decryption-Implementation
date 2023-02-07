# AES-Encryption-and-Decryption-Implementation
-----------------------------------

## About

The Advanced Encryption Standard (AES) is a symmetric block cipher. AES is used to encrypt sensitive data in hardware and software around the world. It developed with a block/chunk size of 128 bits. Using keys of 128, 192, and 256 bits, and transforms each of these individual blocks. This project was a university project under FC421 Applied Cryptography course.

  
--------------------------------------------------------------

## About The Implementation 

By using JAVA language and we have created a class named AES where we defined the functions as methods within this class. First, we gave the user a choice either to encrypt using his own key so he/she should input the message and the key, or an automatically generated random key where he/she only provides the message. We have implemented AES-128 for the key that the user chose and AES-256 for the auto generated key.
We have designed a user-friendly GUI as shown:

![image](https://user-images.githubusercontent.com/122940334/217308112-30905809-1ce0-4871-b1a4-95977c563db4.png)

Once the user clicks on one of the buttons, he/she will be prompted to choose one of another two buttons: 

![image](https://user-images.githubusercontent.com/122940334/217308226-2a09bb2d-20ff-41ff-b9b4-978f79b33057.png)

Based on the buttons the user clicks, the other GUIs will appear. Encryption and decryption with the key of the user’s choice:

![image](https://user-images.githubusercontent.com/122940334/217319827-5403d6d6-695f-423f-898c-cefa8b06f8e5.png)

![image](https://user-images.githubusercontent.com/122940334/217319906-0e0a2a22-599d-4e44-989a-0a9dccd918f0.png)

Encryption and decryption with a generated key:

![image](https://user-images.githubusercontent.com/122940334/217320019-1ec78239-4cab-4e0a-a8fe-4e0a252ca5d8.png)

![image](https://user-images.githubusercontent.com/122940334/217320100-734219de-6730-477a-a5be-5ada22f56b73.png)

The first method defined is the setKey method that is used if the first choice is chosen so we first need to get the key from the user as the plaintext of any length, then we will generate a digest for this input to get a key of 128 bits since AES algorithm requires the key to be 128 or 192 or 256 bits. We used SHA-1 as a hashing function to digest the user key and output the key that would actually be used in the encryption and decryption process.

![image](https://user-images.githubusercontent.com/122940334/217331363-3e66f6b6-2465-47d8-a4db-6668ee357b5c.png)

On the other hand, if the user decided to go with the key generator choice, another method is used which is generating the key. In this method, we have created an object of the class keygenerator and specified the generated key for the AES algorithm, and also specified its length. Then we created an secretkey object where we will store the generated key and used the generator to actually generate a key using generateKey() method, we also converted this key to a string to share it with the user. 

![image](https://user-images.githubusercontent.com/122940334/217331870-dda11f40-243a-475f-a5f8-dc4f2591a384.png)

The third method is the encrypt, this method is called in the encryption GUI when clicked on the encryption button. This method first checked if the user is using his/her own key or the key generator. For the first choice, the setKey() method is called and the input of the user key and the plaintext message is passed as parameters and then the setKey() method is to get the hashed key. In the other case, the generateKey() method is called to create a key. After that, we created an object of the cipher class that is imported and used the getInstance()  method that would implement the specified transformation in the cipher object. AES algorithm with Electronic Code Book mode is specified for this object as shown below along with the padding scheme. Then, the cipher is initialized in the encrypted mode with the created key and then the cipher is used to encrypt the message.  

![image](https://user-images.githubusercontent.com/122940334/217332118-65f714b6-fced-4ccc-b0af-e7f76428866a.png)
    





------------------------------------------------------------------------------------------------------------

## The Future of AES  

Currently, AES algorithm is secure encryption algorithm that is being used heavily in applications to ensure the security and confidentiality of transmitted data. But as we all know, attacks evolve day by day so also security mechanisms against those attacks should improve as well. Quantum computers pose a great threat to most of the encryption algorithms currently in use. The reason behind that is that most of the current cryptographic systems are built on math problems that are hard to solve computationally and these quantum computers can manage large-scale computations (Kristin Lauter, 2018). Hence, many corporates at this time are trying to switch to post-quantum secure encryption techniques. As for AES situation, is predicted that AES- will provide same level of security 256 to the quantum computers attacks as AES-128 currently (What do future advances in technology mean for AES-256 security? 2016). Therefore, it is anticipated that only AES-256 will be implanted and used heavily in applications security and stand against quantum computers threat. Another aspect of AES that requires improvement as well is the slow computations. Especially since AES-256 is slower and would be used mostly. Taking all factors under consideration, it is impossible to anticipate how long would AES still be safe and secure but for the time being, it is still one of best and secure algorithms and would remain in use (What do future advances in technology mean for AES-256 security? 2016). 


--------------------------------------
## Recommendation

some recommendations would be suggested for future work to improve the results of the project.

•	Implementing the two key sizes (128 bits, and 192 bits) for the software program to provide different choices for the users of the program.

•	Using another secure hash algorithm instead of SHA-1 in the key function, for example, SHA-2 or SHA-3, because SHA-1 is already broken so it is not enough secure.

•	Applying the hardware implementation of the AES algorithm using FPGA or ASIC approaches to examine and analyze the different aspects of AES implementations in a better way. 

---------------------------------------

Please hit me up at <a href="https://www.linkedin.com/in/ghaidalamri"> Linkedin</a> if you have any questions or want more details.

    

