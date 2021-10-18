# 12UJavaReviewAssignment

ICS4U1 Review Assignment from Brandon WD. This markdown file is meant to help you get a quick overview of my work, and I have included a .zip file with all the original source files if you wish to take a look in there for further analysis.

## Question 1
Instructions: Write a program that takes in an input. Print the sum of all integers and doubles between 0 and the input value. Place the output in a chart, one for integer and the other for the double. For the doubles, increase the number by 0.1. Implement error checking into your program so that the number entered is greater than 2 (This will make the program more exciting); make sure the user enters an int when prompted and a double when prompted (You might want to put this error checking in a function and put it in a different file for reuse).

Source Code:
```
# Code goes here
```

Sample Output:
```
# Output goes here
```

## Question 2
Instructions:

Source Code:
```
// Question 2 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

// Import java util (all)
import java.util.*;

import java.util.*;

public class Main 
{
public static void main(String args[])
{
    // Create new scanner class called sc; ask user to input string
  Scanner sc = new Scanner(System.in);
    System.out.println("Please enter a word or a phrase:");
    // Scan user input; output string variable one character at a time until completed.
    String str=sc.nextLine();
      for(int i=0;i<=str.length()-1;i++) 
{
      System.out.println(str.charAt(i));
    }
  }
}
```

Sample Output:
```
Please enter a word or a phrase:
java makes my brain hurt
j
a
v
a
 
m
a
k
e
s
 
m
y
 
b
r
a
i
n
 
h
u
r
t

```

## Question 3
Instructions: Write a program that reads input from a given file (ICS 4U Assignment 1.1.txt). Read the file into your program. Have the program count how many characters exist. You are to ignore white space.

Source Code:
```
// Question 3 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

// Import BufferedReader, FileReader, IOException
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Main
{
    public static void main(String[] args)
    {
        BufferedReader reader = null;

        //Initializing charCount to 0

        int charCount = 0;

        try
        {
            //Creating BufferedReader object
            // NOTE: IF YOU OPEN THIS ON ANOTHER DEVICE OTHER THAN MY DESKTOP YOU NEED TO CHANGE THE FILE PATH OR THE PROGRAM WILL NOT RUN!!!!

            reader = new BufferedReader(new FileReader("C:/Users/gogo/Downloads/JavaReviewAssignment/Question_3/TextFile.txt"));

            //Reading the first line into currentLine

            String currentLine = reader.readLine();

            while (currentLine != null)
            {

                //Getting number of words in currentLine

                String[] words = currentLine.split(" ");

                //Iterating each word

                for (String word : words)
                {
                    //Updating the charCount

                    charCount = charCount + word.length();
                }

                //Reading next line into currentLine

                currentLine = reader.readLine();
            }

            //Printing charCount output

            System.out.println("Number Of Chars In The File : "+charCount);

        }
        catch (IOException e)
        {
            e.printStackTrace();
        }
        finally
        {
            try
            {
                reader.close();           //Closing the reader
            }
            catch (IOException e)
            {
                e.printStackTrace();
            }
        }
    }
}

```

Sample Output:
```
Number Of Chars In The File: 1188
```

## Question 4
Instructions:

Source Code:
```
#Code goes here
```

Sample Output:
```
#Output goes here
```

## Question 5
Instructions:

Source Code:
```
#Code goes here
```

Sample Output:
```
#Output goes here
```

## Question 6
Instructions:

Source Code:
```
#Code goes here
```

Sample Output:
```
#Output goes here
```

## Question 7
Instructions:

Source Code:
```
#Code goes here
```

Sample Output:
```
#Output goes here
```
