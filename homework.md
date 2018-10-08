Episode 1
The murderer is Miss Scarlet

Why?
Lexical Scope - accessing scenario.murder variable created outwith function.

Episode 2
Error

Why?
Trying to change a constant

Episode 3
First Verdict:  The murderer is Mrs. Peacock.

Why ?
Murderer changed inside function declareMurderer

Second Verdict:  The murderer is Professor Plum.

Why ?
The variable murderer was declared with let as Mrs Peacock, thus after it has been used by the firstVerdict it is no longer available to the secondVerdict which takes the original value (Professor Plum) which hasn't yet been used.

Episode 4
The suspects are Miss Scarlet, Professor Plum, Colonel Mustard.
Suspect three is Mrs Peacock.

Why?
Same rationale as Episode 3

Episode 5
The weapon is the revolver

Why?
It is possible to change an element of a constant.

Episode 6
The murderer is Mrs White

Why?
murderer is a global variable set by changeMurderer function and then plotTwist function (which is called).

Note - I then added "let" before murderer in the 2 functions and got the response - The murderer is Colonel Mustard.  Is this because these instances of murderer are now not available outwith their functions whereas the first instance (Colonel Mustard) is available due to Lexical Scope?

Episode 7
The murderer is Mr Green

Why ?
I guess because :
  - murderer changed to Miss Scarlet with unexpectedOutcome function
  - Then plotTwist function cannot change murderer to Colonel Mustard because murderer in that function was declared using let so unavailable outwith function
  - so murderer variable reverts to its prior value which was Mr Green as this was declared using a global variable.

  Episode 8
  The weapon is Candle Stick

  Why ?
  Conditions of unexpectedOutcome are met which changes the element scenario.weapon to Candle Stick.

  Episode 9
  The murderer is Professor Plum

  Why?
  Not 100% sure.  Is it because murderer was declared as Mrs Peacock using let and therefore not available outwith block?  Why is Professor Plum available in that case as declared same way ?  Is my confusion down to mis-understanding of definition of block ?
