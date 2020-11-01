Findjmp.c
 written by Ryan Permeh - ryan at eeye - Summarily modified by I2S-LaB.com
 http://www.eeye.com
   
 Findjmp2.c (pop/pop/ret scanner, logging to file)
 version by A.D - class101 at hat-squad
 http://class101.org, http://www.hat-squad.com


 This finds useful jump points in a dll. Once you overflow a buffer, by
 looking in the various registers, it is likely that you will find a
 reference to your code. This program will find addresses suitible to
 overwrite eip that will return to your code.

 It should be easy to modify this to search for other good jump points,
 or specific code patterns within a dll.

 It currently supports looking for:
   1. jmp reg

   2. call reg

   3. push reg
      ret
 All three options result in the same thing, EIP being set to reg.

 It also supports the following registers:
  EAX
  EBX
  ECX
  EDX
  ESI
  EDI
  ESP
  EBP 
