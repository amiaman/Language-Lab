<font color="red"> asr: Whats this file about? is it a copy paste from somewhere? Copy paste are fine as scratchpad but keep them in separate directory like scratchpad, or scrap. In main directory keep only those stuff which you have done yourself. i.e Whatever you have understood, keep that only here. That applies to code as well.
</font>

Compile Command --
                  $ g++ -Wall -save-temps print.cpp -o print
                  
                  So when compile the program print.cpp with -save-temps flag we get the following intermediate files
                  in the current directory (along with the print executable)
                  
$ ls
print.i
print.s
print.o

The preprocessed output is stored in the temporary file that has the extension .ii (i.e ‘print.ii’ in this example)

Now, lets open print.i file and view the content.

I can see that the source file is now filled with lots and lots of information, 
but still at the end of it we can see the lines of code written by us.



After the compiler is done with the pre-processor stage. The next step is to take print.i as input,compile it and produce 
an intermediate compiled output. The output file for this stage is ‘print.s’.The output present in print.s is assembly level
instructions.

Open the print.s file in an editor and view the content.This assembly level output is in some form of 
instructions which the assembler can understand and convert it into machine level language.

At ASSEMBLY stage the print.s file is taken as an input and an intermediate file print.o is produced.
This file is also known as the object file.

This file is produced by the assembler that understands and converts a ‘.s’ file with assembly instructions into a ‘.o’ 
object file which contains machine level instructions. At this stage only the
existing code is converted into machine language, the function calls like printf() are not resolved.

Since the output of this stage is a machine level file (print.o). So we cannot view the content of it.
If you still try to open the print.o and view it, you’ll see something that is totally not readable.


LINKING is the final stage at which all the linking of function calls with their definitions are done














