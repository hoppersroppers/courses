[//]: # (C:\Users\devey\Downloads\backup-moodle2-course-4-the_hard_stuff-20200402-0919-nu-nf\moodle_backup.xml)
[//]: # (35,507,activities/assign_507)
# Hello World
Welcome to the show!
Complete: <https://www.usna.edu/Users/cs/aviv/classes/si485h/s17/units/01/unit.html#lec1>

Do this homework and submit in a text file: <https://www.usna.edu/Users/cs/aviv/classes/si485h/s17/hw/01/hw.html>

---
[//]: # (35,508,activities/assign_508)
# Hello World (The Stack)
Complete: <https://www.usna.edu/Users/cs/aviv/classes/si485h/s17/units/01/unit.html#lec2>

Read: <https://en.wikibooks.org/wiki/X86_Disassembly/Functions_and_Stack_Frames>


---
[//]: # (35,378,activities/assign_378)
# Hello World (Objdump)
Alright you wrote the C.

Follow this tutorial up to the end of part 3. 
<https://www.usna.edu/Users/cs/aviv/classes/si485h/s17/units/02/unit.html> 

---
[//]: # (35,380,activities/assign_380)
# Hello World (GDB)
Print this cheatsheet and hang it up behind your computer:
<http://users.ece.utexas.edu/~adnan/gdb-refcard.pdf>
If you can't print it, just save it. 

Follow this tutorial:
<https://beej.us/guide/bggdb/>

Play around with GDB and submit the location and values of the part of memory that contains the string "Hello, world".

---
[//]: # (35,379,activities/assign_379)
# Hello World (Manual Compilation)
So you wrote it in C and it compiled.... but what is compilation? 

<http://cs-fundamentals.com/c-programming/how-to-compile-c-program-using-gcc.php>

Use ccp to convert your source code .c to a .i file.

Then use gcc to convert your .i file into a  .s  file. 
Submit your .s file.

Then use as to convert your .s file into a .o binary.
Submit your .o binary.

Then use ld to build an executable file. I hate to break it to you, but the example in the text above will not work. Why will it not work? Likely because the names of the required libraries will be different or in different places, depending on your OS. So how would we figure this out? Look at this link and try to figure out what crt is. <https://en.wikipedia.org/wiki/Crt0>

So let's cheat and just use GCC.  
<https://www.computerhope.com/unix/uld.htm>

You can try to just do it yourself but it's really boring and just spends a lot of time trying to find out where everything is. 

Execute that file and confirm success.

---
[//]: # (35,383,activities/assign_383)
# Hello World (Linking)
We cheated on linking last time.... 
Time to do it yourself.

<https://blogs.oracle.com/linux/hello-from-a-libc-free-world-part-1-v2> 

<https://blogs.oracle.com/linux/hello-from-a-libc-free-world-part-2-v2>

---
[//]: # (35,381,activities/assign_381)
# Hello World (Ghidra)
Alright you wrote the C.
Welcome to Ghidra.

Send us a screenshot of it in Ghidra.



---
[//]: # (35,382,activities/assign_382)
# Hello World (IDA)
Alright you wrote the C. You used Ghidra. Guess what, Ghidra can't do everything, and you should know how to use the undisputed champ. 

Welcome to IDA.

Send us a screenshot of it in IDA.



---
