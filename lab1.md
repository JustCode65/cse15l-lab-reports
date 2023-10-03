# **LAB REPORT 1**
***

1. cd (Change Directory)
   * Ex 1: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cd1.PNG)
   * There was no directory selected
   * Nothing really happened since I didnt put any directory argument
   * It was not an error because nothing happens with just cd as a command
  
   * Ex 2: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cd2.PNG)
   * There was no directory selected
   * It accessed the lecture1 directory since lecture1 is an accessible directory
   * It was not an error because it successfully accessed the lecture1 directory
  
   * Ex 3: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cd3.PNG)
   * The working directory was in the messages directory, which was in the lecture1 directory
   * It returned a statement that tells the user that ko.txt was not a directory. cd only works with directories. not text files.
   * It was an error because bash returned a statement. It told the user to not use text files as a diectory.
  
2. ls (List)
   * Ex 1: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/ls1.PNG)
   * There was no directory selected
   * It returned the name of a directory, lecture1, since lecture1 is the only thing to list
   * It was not an error because the command, ls, was used correctly.
  
   * Ex 2: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/ls2.PNG)
   * There was no directory selected
   * It returned the names of all the files in lecture1
   * It was not an error because it successfully listed all the files in lecture1 and was used correctly.
  
   * Ex 3: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/ls3.PNG)
   * The working directory was in the messages directory, which was in the lecture1 directory
   * It returned the name of the file, ko.txt
   * It was not an error since the ls command was used correctly. It fufilled its purpose by returning the name of the file, ko.txt
  
3. cat (Concatenate)
   * Ex 1: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cat1.PNG)
   * There was no directory selected
   * It didnt return anything. However, it recieves a user input and return it back to the user until the user decides to end it with CrtlD.
   * It was not an error because the cat command still accepts inputs from the user without crashing. However, the user does need to end the program.
  
   * Ex 2: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cat2.PNG)
   * There was no directory selected
   * It returned a statement that says that lecture1 is a directory. The cat command only really be used with files.
   * It was error because bash  returned a statement that says that lecture1 is a directory.
  
   * Ex 3: ![Image](https://github.com/JustCode65/cse15l-lab-reports/blob/main/lab1_pics/cat3.PNG)
   * The working directory was in the messages directory, which was in the lecture1 directory
   * It returned the contents of the file in ko.txt
   * It was not an error since the ls command was used correctly. It fufilled its purpose by returning the contents of the file.
