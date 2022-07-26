# Notes about regular expressions!

## _Delimiters_

. Find all characters
\*  There are  zero or no characters
\+  Find one or more characters
?  Find zero or one characters

### Example
```sh
1
12
123
```
If we make a regex = * , It will find all characters in the three lines
The same result we get if we make a regex = .* 


```
1 
12
123
1234
12345
12345678910
12345678910a
13453243
url: https://www.onepage.com/p/BXB4zsUlW5Z/?token-by=some.mx
url: http://instagram.com/any-expresion/blablablah
http://instagram.com/p/blablablah
Alexander Cardenas
```

### Practice

Copy last piece of code and write the next regular expression in your favorite editor - I recommend Atom and enable regex browser, press Ctrl + F and push on regex option

_Regex to practice_

-  ``` \d+[a-z]```   Get all ocurrences when regex find at least one digit followed by letters
    In this case match: 
```
12345678910a
url: https://www.onepage.com/p/BXB4zsUlW5Z/?token-by=some.mx
```
At the secon line match on ```4z``` and ```5Z```

Other important commands are:
- ```\w``` : Find letters, including (-) and (.) characters
- ```\s``` : Find spaces

## Use NOT or negation

To use negation expresion there are diferent posibilities, look
- ```\D``` : Find all characters except digits
- ```\W``` : Find all characters except letters, (-) and (.) characters
- ```\S``` : Find all characters except spaces


## Begin (^) and Ending of Line ($)

To find a line where there is only one digit we can use this two new characters. how to do? ... let's go!
```
1 
12
123
1234
12345
12345678910
12345678910a
13453243
url: https://www.onepage.com/p/BXB4zsUlW5Z/?token-by=some.mx
url: http://instagram.com/any-expresion/blablablah
http://instagram.com/p/blablablah
Alexander Cardenas
```
Using this example one more time, we will find a line with only one digit as follows:
-  ``` ^\d$ ```
This expression match if begin the line, next find one digit and finally end the line.

If we wanted to find two digits between the begining and the ending, we can use:
- ``` ^\d{2,2}$```
This expression match te second line, since it fulfills the conditions.
