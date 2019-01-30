# Exploring-.padStart-

This is an example that shows a couple lines of code for a basic example of .padStart(), and then an example that gets a little
more involved. This is based off the MDN entry on .padStart(), found here: 
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padStart

The goals of this example are to:
• Explain how .padStart() works  
• Show a basic use of .padStart()  
• Make a function that takes a 16 digit credit/debit card number and report that said   
number was successfully charged. If the number isn’t 16 digits, we should inform the customer as such. 

The .padStart() method is used to extend the length of a calling string to a certain value.   
Note that the string to be added will be added on the left side of the calling string, meaning that it will be   
the beginning of the newly made string. This method takes two arguments: the first being the desired length of the   
new string to be made, and the second being the string to be added. The original string remains unchanged.  

Note that padString in the case of .padStart() is added to the LEFT side/BEGINNING of the calling string.   
If you want stuff added to the end/right side of the calling string, in a similar fashion, use .padEnd().    

In the first example, we make our reveal string 25 characters long by adding a period encased in a string ‘.’  to the left side   
of reveal until reveal is 25 characters long.  

The second example is a little more complex. We make a var numString which just adds an empty string to our num argument.   
Then, we use an if statement saying that if this string is exactly 16 characters, use .splice(-4) on it to create the var last4,   
which is just the last 4 characters of numString. Then, we take last4 and use .padStart(16, ‘\*’) to add asterisks to the beginning of last4
until it’s 16 characters long. We then use a template literal including that process to make a sentence stating the card was successfully 
charged. We see that if num is not 16 digits/characters, we get a message saying to make it so.

Notes pertaining to the second example:
• (We’re not going into a function that would actually link to the card’s account, etc, just displaying a message)
• This example does not cover if the argument can be made into a string that doesn’t contain numbers. \
(ex. If you put something like “1111222233344x4”, it will pass in this example).
