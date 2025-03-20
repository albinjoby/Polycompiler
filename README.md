# polycompiler

The polycompiler is a compiler that can contain and run 2 or more languages.

In this case I am implementing this in python and javascript

implementation 1:

in python we use :
1 // (lambda:print("python") or 1)()

In Python, the compiler prints “hello world” because the lambda function is invoked immediately. The or operator ensures that the function returns 1, even though print('hello world') itself returns None. The lambda function is enclosed in an immediately invoked function expression (IIFE), meaning it runs as soon as it is defined.

meanwhile when node js reads the code it sees 1 and then a comment //(lambda:print("python") or 1)() which means teh rest of the part does not execute since // is consider as the begining of a comment

in javascript we use:
lambda: eval("console.log('hello world')")

in javascript lambda: is considered as a label and is run

mean while in pthon the keyword lambda is used a through away funcion

do note that eval in both languages is used to convert the given string into code dynamically