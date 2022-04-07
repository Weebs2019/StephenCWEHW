* What CWE am I writing about?
	* CWE-20 imporper input validation

* How was my code vulnerable to it?
	* Going back to files from my old coding days, i came across code that if executed would be vulnerable
as it fits the description of CWE-20 (Improper input validation). Improper input validation is when the code
accepts an input that is not supposed to be accepted based on the situation. This could be a negative number
entered when only positive numbers should be accepted or when certain types of characters should not be
accepted (i.e. letters are supposed to be denied but are still accepted by the code or they terminate the
program).   

		My code needed to compare how much money would be in two people's savings accounts in
a certain amount of time. The user could enter the initial deposit and interest rate for both people. Once all
the information was entered for both people, the number of years was entered for how many years are allowed to
grow. After the number of years was entered, the output displays which person has how much more money than the
other person. The weakness is where the input does not check if negative numbers were entered in at any point of
entering in numbers.

	  The code is has no system of checking for negative numbers. A major fix that I would add to fix all of the
issues is to use an if-else sequence in a loop to check that the inputs are valid, AKA check to that all the values are positive numbers. If they are invalid (i.e. 
negative numbers or non-numeric characters, with the exception of "," and "."), then the code would keep asking 
for valid inputs or let the user end the program and exit.
