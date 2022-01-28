## Week 4 Lab Report

# First code change
The first bug that was found in the code is that if there are no open brackets, the code will have a symptom be in an infinite loop. This is because as long as the current index is less than the length of the markdown, the while loop will continue to run. Since the open bracket is not there, the `indexOf` command will give out -1. This will lead the `currentIndex` to never increase to the markdown length and thus be stuck in an infnite loop. To fix this, my group adds a conditional statement where if the open or close brackets are not found, then the code will automatically close.

# Second code Change
The second bug that was found in the code is that empty text, with no brackets or parenthesis, will lead to a symptom of index out of bounds error. This is because since the `indexOf` command will return -1 if it cannot find the given argument. In the code that was given in class, it will add to the return value the substring of open and close Paren. But since both of the parenthesis is not there, it will try to find the substring of -1, which will not work. A solution will be to have a conditional where it will end the loop early if cannot find either of the parenthesis.

# Third code Change
The third bug that was found in the code is the issue of valid links. A link is not valid if it has a space. But, in test file 5, adding a space to a link will lead to the link to be printed out, even though if it's not valid. To fix the symptom of having invalid links with space, my group decided to have the solution where if there is a space within the parenthesis, the program will skip that specific bracket and go on to the next link in the file.