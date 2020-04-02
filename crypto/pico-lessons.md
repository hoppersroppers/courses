# Introduction to Cryptography with picoCTF (I/P) #

Please note that this section of the course is still in progress.

## General ##

In this section of the course, we are going to use the excellent 2019 picoCTF to learn some of the fundamental concepts of cryptography. picoCTF is a CTF designed by an [excellent team of security experts at Carnegie Mellon University](https://picoctf.com/about) with the goal of introducing beginners to a wide variety of security topics. You can sign up and start working on challenges [here](https://2019game.picoctf.com/). We recommend starting cryptography with these challenges because they practical, approachable, and hands-on. You do not need to know anything about cryptography to get started!

While we try to have as few prerequisites as possible, you will have to have a little experience with using command lines and programming to get through this course. We found that Linux and python worked well for these challenges, but many other languages and OSes will likely work with a few modifications as well. If you are completely new to command lines or programming, or you just want to brush up on these skills, check out the Hopper's Roppers **Introduction to Computing Fundamentals** and **Essential Practical Skills** courses. 

Also, modern cryptography is based on math. Often, the concepts and terms are not familiar to people before they start learning about cryptography. Don't let this deter you! If you take the time to break down the new concepts, you'll often find that they are much simpler than they initially seemed. And, as with everything else, please do not hesitate to reach out if you have any questions.

For now, the most important math to be familiar with is modular arithmetic. While that term might be new to you, we promise that you already use modular arithmetic whenever you use a clock. Khan Academy has a good introduction [here](https://www.khanacademy.org/computing/computer-science/cryptography#modarithmetic). 

Finally, before you jump into the challenges, we recommend quickly skimming [picoCTF's own cryptography reference](https://picoctf.com/learning_guides/Book-2-Cryptography.pdf). You don't have to sweat every detail right now. Focus more on getting an overall sense of the topics in there.

The following sections have information to supplement the picoCTF challenges. Our goal is to put the challenges in context and emphasize the most important takeaways to ensure that you can learn as much as possible from them. We are not providing solutions. If you get stuck or have questions, feel free to reach out to the Hopper's Roppers educators (start with @inzano in the Discord) or community. You can find solutions elsewhere on the Internet, but, if you look those up, you will miss out on the lessons learned in working through the challenges yourself.



## 00 The Numbers ##

The Numbers relies on obscuring the flag through some unknown encryption scheme. With some perseverence and trial and error, you can figure out the scheme. Once you do, it will be straightforward to figure out the flag. 

No fancy techniques or math involved here. You know that the flag starts with `PICOCTF{` and ends with `}`. Think about how these numbers could reflect that.

Check the hint. Capitalization matters. Attention to formatting is essential here, as well as in CTFs and infosec at large.

Once you're done, read [this wikipedia discussion of Kerckhoff's Principles](https://en.wikipedia.org/wiki/Kerckhoffs%27s_principle). These first few problems will hopefully help you see for yourself why professional cryptographers are so adamant about Kerckhoff's Second Principle.



## 01 13 ##

If you do not already know what ROT13 is, then this challenge tests perhaps the most crucial skill to CTFs: searching online and learning on the fly. Seriously.

CTF authors do not expect contestants to already understand everything they need to know right away. Ideally, they will give you just enough information to prepare you to teach yourself whatever it is you need to know. This is an incredibly important skill to information security practictioners, because they will constantly come up against technologies and concepts that they have never dealt with before.

As a general rule, whenever you come up against something you do not understand in one of these challenges, try searching for it. If the first few resultsdon't help, keep searching. If the results contain more concepts you don't understand, consider searching for them, too. It may seem overwhelming or daunting, but we promise that patience, perseverence, and a willingness to learn go a long way.

Additionally, once you figure out what ROT13 is, you may find that you can solve this challenge by hand. However, you may also find that it would be quicker to write a script or find a free online tool to quickly do it for you.



## 02 Easy1 ##

As with before, do not forget to search for any term you do not already understand. And do not hesitate to read the hint.

By the way, the picoCTF authors are absolutely correct that One Time Pads theoretically offer perfect confidentiality. They reason we do not use them is because they are impractical: OTPs must be at least as long as the message they encrypt, and adversaries cannot know anything at all about their composition. As a result, sharing an OTP with someone you trust is no easier than just sending them the sensitive message that you want to encrypt.



## 03 caesar ##

The Caesar Cipher is probably the most famous pen and paper cipher out there. Read the hint, and consider reading about it in the picoCTF cryptography guide as well. 

If you have not already done so, this would be a great time to learn about [modular arithmetic](https://www.khanacademy.org/computing/computer-science/cryptography#modarithmetic). Getting used to this math will really help you understand this cipher and will pay dividends in the challenges to come.

As you approach this challenge, think about the size of the Caesar Cipher's _key space_, or the set of all possible keys. In almost all cryptosystems, the security of the cryptosystem relies in large part on the size of the key space. If there are few enough possible keys that an attacker can _brute force_ it, which means simply trying all the possible keys, then the attacker can get the sensitive message by just doing that. 

On a possibly related note, you could solve this challenge by hand, but it is going to be much faster to use a computer to help out. Try finding a tool online or programming one yourself.



## 04 Flags ##

This challenge should further demonstrate to you the value of Kerckhoff's Second Principle. If your cryptosystem relies on keeping the mechanics of the system secret, well, it is probably only a matter of time before the adversary figures out those secrets and is able to read your messages.

(Of course, the flags used to "hide" the secret message here will not be secret at all to many of the Sailors working on this challenge.)

As always, pay attention to the hint and the format that you use to submit the flag.



## 05 Mr-Worldwide ##

If you have not already done so, this challenge is your opportunity to prove to yourself that you can uncover the method behind an ad hoc encoding scheme through patience, perseverence, and some trial and error. 



## 06 Tapping ##

This is the first challenge that explicitly calls for the use of a command line utility. On many Unix-like machines, `nc` is netcat. If you're on Windows, you will have to install netcat yourself.

This challenge is very similar to the last couple challenges: the data in encoded in a way that is not immediately readable, and it is up to you to figure out what that encoding scheme is.

As always, check the hints and be careful about formatting.



## 07 la cifra de ##

Read the hints, think about them carefully, and do not hesitate to use DuckDuckGo or Google! You might also peruse picoCTF's cryptography guide, too.

This one would be extremely difficult, if not impossible, to solve without some computational tool. 

This might be a good time to point you to [boxentriq](https://www.boxentriq.com/code-breaking/cipher-identifier), an absolutely awesome resource for classical ciphers.



## 08 RSA pop quiz ##

### RSA ###

This is the first challenge to rely on a modern cryptosystem! To solve this challenge, you will have to learn about RSA.

Yakuhito has an excellent introduction to its mechanics on his blog [here](https://blog.kuhi.to/rsa_encryption_signatures_and_blind_signatures). We recommend you start there.

If you want, this would also be a great time to brush up on [modular arithmetic](https://www.khanacademy.org/computing/computer-science/cryptography#modarithmetic).

[picoCTF's cryptography reference](https://picoctf.com/learning_guides/Book-2-Cryptography.pdf) has some good information on RSA to read as well.

And, as always, don't hesitate to use your favorite search engine to learn more.

### Coding Tips ###

Unlike the previous challenges, this one definitely calls for you to write some code. 

Whatever language you choose, make you are setting it up to handle very large integers without losing precision. Python can accomplish this easily. 

If you are using python, you would be wise to install [PyCrypto](https://www.dlitz.net/software/pycrypto/). This is the go-to python library for all things crypto. There are a couple ways to install it; I used `aptitude install python-crypto` and `aptitude install python3-crypto`.

There are a ton of useful features in this library. For this challenge, you might want to get comfortable with the `Crypto.Util.number` library. The `long_to_bytes` and `bytes_to_long` functions, which convert between interpreting data as large integers and ASCII strings. Also, `inverse` is useful for calculating modular inverses.



## 09 miniRSA ##

RSA is secure if you implement it just right, but this is much easier said than done. This challenge, along with several of the subsequent challenges, will have you look carefully at various parts of the RSA cryptosystem to uncover how the whole thing breaks if there are minor modifications or errors made in implementing it.

Think about the hints to this challenge, read the Wikipedia article, and carefully examine the size of the given `e`, `N`, and `c`, as well as the equation for encryption.

Don't forget about the coding skills you used in the last challenge. Also, if you do not have an algorithm for a calculation you want to make, don't hesitate to search for it online. There's a lot of code on stack exchange.



## 10 waves over lambda ##

Here, we are going back to classical ciphers. It is up to you to figure out which one this is and decode it. Don't forget about the resources discussed for the previous challenges.

While you are at it, we highly recommend you take a look at this introduction to [frequency analysis](https://crypto.interactive-maths.com/frequency-analysis-breaking-the-code.html).  

Please heed the hint about the flag format.



## 11 b00tl3gRSA2 ##

Here is another RSA challenge. As always, look at the hint. If you are unsure what values are typically used for `e`, we highly suggest you search online and consult resources you've already looked at for RSA.

To address the description itself, there are tradeoffs for the number chosen as `e`. Too small, and you run the risk of vulnerabilities like those in miniRSA. However, the bigger that `e` is, the slower the modular exponentiation in the encryption. In practice, you want the smallest `e` you can get away with that doesn't sacrifice security.

As an aside, the RSA in these challenges is "textbook" RSA. State-of-the-art RSA has multiple refinements that make it even faster (for the legitimate parties) and more secure. If you want to learn more, read [this great stack exchange post](https://crypto.stackexchange.com/questions/1448/definition-of-textbook-rsa) and dig into the links it contains. You could also read about [Optimal Asymmetric Encryption Padding](https://en.wikipedia.org/wiki/Optimal_asymmetric_encryption_padding).

## 12 AES-ABC ##

### Block Ciphers ###

With this challenge, we are taking a break from RSA and looking at [block ciphers](https://www.tutorialspoint.com/cryptography/block_cipher.htm).

The foundation of block ciphers is the base encryption algorithm. There are many variations, but two very good ones are [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) and [3DES](https://en.wikipedia.org/wiki/Triple_DES). All these base algorithms take a single "symmetric" key that is used for both encryption and decryption (unlike the public and private keys that are used for asymmetric encryption such as RSA.) They then use this key to encrypt (or decrypt) a "block" of a very specific size. For instance, AES can use keys that are either 128, 192, or 256 bits, and handles blocks of exactly 128 bits. 

But what if you want to want to encrypt something that is not exactly 128 bits? If you want to encrypt something very small, you can "pad" your message with junk bits until it 128 bits long. (There are lots of ways to do this.)

If you want to encrypt something longer, that's where block ciphers come into play. Block ciphers divide what you want to encrypt into a bunch of blocks, and use the base encryption algorithm to encrypt each one. The simplest way to do this is to simply encrypt each block with the key, doing nothing else. This mode, called ECB (for "electronic cookbook") ensures that each block is individually securely encrypted, but it does not hide patterns throughout the data, because blocks that are repeated will always encrypt to the same cipher block. Ilmari Karonen provides a great discussion of this in [this post](https://crypto.stackexchange.com/questions/20941/why-shouldnt-i-use-ecb-encryption) talks about why this is important.

To combat this, cryptologists have developed a number of "modes" of block ciphers which address the weaknesses in ECB. The previous link talks about some of them. In this challenge, the author comes up with her own mode called "ABC" mode to try to do just this.

### Schneier's Law ###

Whenever someone says they are writing their own crypto system, whether for CTFs or otherwise, you should assume it is insecure. Renowned cryptologist Bruce Schneier put it this way:

> Anyone, from the most clueless amateur to the best cryptographer, can create an algorithm that he himself can't break. It's not even hard. What is hard is creating an algorithm that no one else can break, even after years of analysis. And the only way to prove that is to subject the algorithm to years of analysis by the best cryptographers around.

This quote has become so widely regarded in the cryptologic community that people simply refer to it as [Schneier's Law](https://www.schneier.com/blog/archives/2011/04/schneiers_law.html). You might think of it as the Moore's Law of cryptology. People sometimes just summarize and say "don't roll your own crypto."

We are not going to get into a full discussion of this guidance here. Our hope is that, by the time you finish all the crypto content in Hopper's Roppers, you will have convinced yourself of the wisdom of Schneier's Law.

This challenge is a great opportunity to see how quickly custom crypto can fall apart. Look at the provided code. As the challenge hint suggests, see if you can reverse the custom crypto and get the image back to ECB encryption only.



## 13 b00tl3gRSA3 ##

The security of RSA depends on the difficulty of factoring `n`. Typically, `n` is the product of just two (large) primes `p` and `q`. This challenge pushes you to explore what happens to the difficulty of factoring when more primes are involved.

Multi-prime RSA is indeed an accepted standard alternative to traditional RSA. When used correctly, it can still be secure while offering ways to decrypt quickly. Of course, it is not used correctly in this challenge. The mechanics are overall pretty similar, but, as the challenge hint suggests, you will have to reconsider how `d` is calculated. We are not going to give the full details here; that is the challenge for you to search for and figure out yourself!

It could be a good exercise to try to write your own program to factor the `n` given in this problem. However, you should know that there are some phenomenal programs that are freely available that use state of the art techniques to attempt to factor large numbers as quickly as possible. Here are some of our personal picks:
- [yafu](https://sourceforge.net/projects/yafu/) is an awesome program you can run on your own computer. 
    - note that yafu is best for factoring a product of two large primes. It can handle some more primes, but sometimes it stops when it has only found some of the factors. Watch out for the line `too many refactorization attempts, aborting`.
- [Alpertron's online tool](https://www.alpertron.com.ar/ECM.HTM) is also seriously worth checking out. You can run it in your browser. Not only does it factor large numbers, it also calculates some other useful things about the large number, like the totient.

You have to be pretty careful as you go through this challenge. If you are not getting the results you expect, make sure to double and triple check everything. Be careful about how you implement any math formulas you find. Also, as with the other problems, ensure that you are handling the large integers without losing any precision. (Trying to use floats will almost certainly sacrifice precision.) As always, perseverence with your online searches and attention to data formatting are essential.



## 14 john_pollard ##

### A Brief Introduction to Digital Certificates ###

Up until this point, all of the cryptography challenges in picoCTF have only dealt with hiding secret information. This final challenge is a brief introduction to the wide world of cryptography that aims at providing other sorts of security guarantees. 

Specifically, this challenge will have you examine a digital certificate. Certificates are used for _authentication_, which means that they help someone providing information verify that they are who they say they are. When you go to a website and see a little green padlock next to the website URL (say, `https://www.navy.mil`), that means that the website operators (here, the US Navy) are using a certificate to help show that they are indeed serving the website and that some imposter is not just pretending to be the Navy. The same logic applies when you use a CAC to log in to a website, when you use a certificate to sign an email, or when you sign a PDF.

The heart of this security is based on the secrecy of the signer's private key. If you use RSA, that is `d`. If you have a private key and someone steals it, that person can sign things in your name!

There is a lot more that goes into [digital certificates](https://en.wikipedia.org/wiki/Digital_signature) than we will get into here. If you want to learn more, you will want to learn about, among other things, [hashing](https://en.wikipedia.org/wiki/Cryptographic_hash_function) and [certificate authorities](https://en.wikipedia.org/wiki/Certificate_authority) along the way. The reality of digital certificates today is very complicated and messy. Even if everyone does the math perfectly, there are still a ton of existing weaknesses in the digital certificate system. Of course, [people still make critical errors with the math, too](https://media.defense.gov/2020/Jan/14/2002234275/-1/-1/0/CSA-WINDOWS-10-CRYPT-LIB-20190114.PDF)! 

### The Challene ###

This challenge presents you with a vulnerable [X.509](https://en.wikipedia.org/wiki/X.509) certificate. You know from the description and hints that it was created using RSA and that you will need to figure out which primes `p` and `q` are associated with it. 

The first step, of course, is figuring out how to read the certificate. If you open it up in a text editor (try it!), you'll quickly see that it is not stored in a human readable format. There are a lot of ways to get open the certificate in a human-readable format. (Hint: this is a good time to get familiar with the `openssl` tool for Linux.)

From there, you will need to figure out how to determine the `p` and `q` associated with the certificate. The primes themselves cannot be stored in the certificate; if they were, anyone could figure out the secret key `d`. Use what you have learned about RSA so far to see if you can calculate these prime numbers.
