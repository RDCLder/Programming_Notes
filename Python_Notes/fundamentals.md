WINDOWS Command Line Fundamentals

•	The PowerShell is the command prompt for windows OS
o	An OS is structured like a tree in which a root directory can then branch off into subdirectories (e.g. folders, files, etc.)
	Root directory is C:
	Levels of the hierarchy are separated by \
	Home directory is designated by ~ and is usually C:\Users\Username

o	The command prompt has greater functionality than a GUI like Windows Explorer
	e.g.  Instead of manually dragging a file from directory to directory, PowerShell can perform that function with a line of code

•	PowerShell has several basic functions that can be used to manipulate files
o	Basic directory functions
	cd	addresses the current directory
	..	goes back one level to parent directory (e.g. cd ..)
	ls	lists all the contents of current directory
	wpd	lists the exact path from root directory to current directory
	~	accesses the home directory

o	Other functions
	clear	clears current PowerShell text

•	Creating Directories
o	mkdir command can make new directories
	syntax:  mkdir folder
	This will create a new folder called “folder” in the current directory

•	Creating Files
o	



Getting to Know Python

•	print function can use both apostrophes (‘) and quotation marks (“) to denote strings
o	If you use both (‘) and (“) in a print function such as in the following example:
print(‘The pet shop owner said “No no, ‘e’s uh,… he’s resting” ’)
o	You can add backslash (\) in front of the marks you opened the string with (in this case apostrophes) to allow the function to interpret the mark as a string
o	e.g. \’e\’s will cause the interpreter to recognize the apostrophes as part of the string

•	Highlighting code and pressing Ctrl + / will convert code to comment


Understanding More About Python

•	print function can add the same elements together in parentheses
o	e.g. print(‘string 1’ + ‘string 2’)
o	e.g. print(2 + 2)

•	print function cannot add strings and numbers (integers or floats) together by itself.
o	e.g. print(‘string’ + 2) will cause an error

•	Strings can be split by backslash commands
o	e.g. \n will cause the proceeding string to start on a new line
o	e.g. \t will cause the proceeding string to start after a tab indent

•	Triple quotes/apostrophes will allow you to split a string over multiple lines in the same way that the \n command will
o	e.g. ‘’’string 1
string 2
string 3‘’’
o	This will allow you to mix both quotation marks and apostrophes without worrying about syntax as everything contained inside the triple quotes/apostrophes will be considered a string


Storing Items in Variables & More About Variables and Strings

•	Variables can be named starting with letters and underscores but not numbers
o	Variable names can still contain numbers, just not at the beginning
o	e.g. _author_, greeting, tim, Tim, Tim45

•	Data types include strings, integers, floats, and complex numbers
o	Strings are contained within apostrophes/quotations and can include any character
o	Integers are real, whole numbers and do not include decimal points/fractions.
o	Floats are real numbers that can include decimal points/fractions
o	e.g. 4 is an integer while 4.0 and 4.1 are both floats
o	Dividing with / operator returns a float with decimals.  Double // are needed to return an integer.
o	A string can be multiplied by an integer to return multiples of the same string

•	For variables, i notation is formatted as follows: [start:stop:step]
o	The count starts at 0 instead of 1
o	The stop means up to and not including (e.g. [1:3] would include 1 and 2 only)
o	The step can be negative and the stop can be lower than the start
o	Blanks direct to default options: start at zero, stop at end, step of 1

•	In a for loop, the range is formatted as: 
o	for i in range():


String Formatting – Displaying Numbers And Strings

•	str function can convert a number to a string

•	Replacement fields are a function that replaces every instance of {} inside a string with a specified element.
o	Formatted as ‘string with {}’.format(e1) where the elements contained within the parentheses of .format() replace the curly brackets {}.
o	Elements can be specified inside curly brackets: {0} will be replaced with the first element of the .format()
o	e.g. print(‘January has {0} days while April has {1} days.’.format(31, 30))
o	The above code will replace {0} with 31 and replace {1} with 30.
o	Elements inside the parentheses can be numbers, strings, or variables
o	Elements can be repeated if curly brackets are repeated
o	Replacement fields can also denote space: {0:2} denotes the first element with 2 spaces
o	{0:<4) denotes up to 4 spaces and justifies the result to start from the left until it goes to the fourth space

•	F-Strings are a way to format strings in which {} can include variables
o	Syntax:  f’str {variable}’
o	e.g.  f’My age is {age}.’

•	% operators can be used to fulfill the same purpose as a replacement field
o	Formatted as % + number + element type where the number sets amount of spaces
o	e.g.  print(‘Pi is approximately %12f but we’ll use %2d’ %(22 / 7, 3))
o	%12f denotes 12 spaces and a float element while %2d denotes 2 spaces and an integer
o	The default accuracy for floats is six decimal places, but the accuracy can be changed by adding a period and a number
o	e.g. %12f.50 would denote an accuracy of 50 decimal places for 22 / 7
