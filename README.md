# 12UJavaReviewAssignment

ICS4U1 Review Assignment from Brandon WD. This markdown file is meant to help you get a quick overview of my work. If requested, I can send a .zip file with all the original files and images.

## Question 1
Instructions: Write a program that takes in an input. Print the sum of all integers and doubles between 0 and the input value. Place the output in a chart, one for integer and the other for the double. For the doubles, increase the number by 0.1. Implement error checking into your program so that the number entered is greater than 2 (This will make the program more exciting); make sure the user enters an int when prompted and a double when prompted (You might want to put this error checking in a function and put it in a different file for reuse).

Source Code:
```
// Question 1 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

import java.util.Scanner;

class Main
{
public static void main(String[] args)
{
  // Create variables
  int userInput;
  String tempUserInput;
  // Scanner used to take user input
  Scanner scan = new Scanner(System.in);
  System.out.println("Please enter the number you wish to end on");
  //While loop with try/catch
  while(true)
  {
    try
    {
    System.out.print("Enter an integer greater than 2: ");
    tempUserInput = scan.nextLine();
    userInput = Integer.parseInt(tempUserInput);
    if(userInput > 2)
    {
      break;
    }  
    else
    {
      System.out.println("The number you entered must be larger than 2.");
    }
    }
    catch(Exception e)
    {
      //Left blank, no action needed
    }
  }
  System.out.println("Integer\t\t\t\tDouble\n______________________________");
  //This for loop is for integer values & doubles at #.0
  for(int counter = 0; counter <= userInput; counter++)
  {
    System.out.println(counter+"   \t\t\t\t"+counter+".0");
    for(int decimal = 1; decimal <10; decimal++)
    {
      if(counter == userInput)
      {
        break;
      }
      System.out.println("         \t\t\t\t"+counter+"."+decimal);
    }
  }
}  
}
```

Sample Output:
```
Please enter the number you wish to end on
Enter an integer greater than 2: 60 9
Integer				Double
______________________________
0   				0.0
         				0.1
         				0.2
         				0.3
         				0.4
         				0.5
         				0.6
         				0.7
         				0.8
         				0.9
1   				    1.0
         				1.1
         				1.2
         				1.3
         				1.4
         				1.5
         				1.6
         				1.7
         				1.8
         				1.9
2   				    2.0
         				2.1
         				2.2
         				2.3
         				2.4
         				2.5
         				2.6
         				2.7
         				2.8
         				2.9
3   				    3.0
         				3.1
         				3.2
         				3.3
         				3.4
         				3.5
         				3.6
         				3.7
         				3.8
         				3.9
4   				    4.0
         				4.1
         				4.2
         				4.3
         				4.4
         				4.5
         				4.6
         				4.7
         				4.8
         				4.9
5   				    5.0
         				5.1
         				5.2
         				5.3
         				5.4
         				5.5
         				5.6
         				5.7
         				5.8
         				5.9
6   				    6.0
         				6.1
         				6.2
         				6.3
         				6.4
         				6.5
         				6.6
         				6.7
         				6.8
         				6.9
7   				    7.0
         				7.1
         				7.2
         				7.3
         				7.4
         				7.5
         				7.6
         				7.7
         				7.8
         				7.9
8   				    8.0
         				8.1
         				8.2
         				8.3
         				8.4
         				8.5
         				8.6
         				8.7
         				8.8
         				8.9
9   				    9.0
         				9.1
         				9.2
         				9.3
         				9.4
         				9.5
         				9.6
         				9.7
         				9.8
         				9.9
10   				    10.0
         				10.1
         				10.2
         				10.3
         				10.4
         				10.5
         				10.6
         				10.7
         				10.8
         				10.9
11   				    11.0
         				11.1
         				11.2
         				11.3
         				11.4
         				11.5
         				11.6
         				11.7
         				11.8
         				11.9
12   				    12.0
         				12.1
         				12.2
         				12.3
         				12.4
         				12.5
         				12.6
         				12.7
         				12.8
         				12.9
13   				    13.0
         				13.1
         				13.2
         				13.3
         				13.4
         				13.5
         				13.6
         				13.7
         				13.8
         				13.9
14   				    14.0
         				14.1
         				14.2
         				14.3
         				14.4
         				14.5
         				14.6
         				14.7
         				14.8
         				14.9
15   				    15.0
         				15.1
         				15.2
         				15.3
         				15.4
         				15.5
         				15.6
         				15.7
         				15.8
         				15.9
16   				    16.0
         				16.1
         				16.2
         				16.3
         				16.4
         				16.5
         				16.6
         				16.7
         				16.8
         				16.9
17   				    17.0
         				17.1
         				17.2
         				17.3
         				17.4
         				17.5
         				17.6
         				17.7
         				17.8
         				17.9
18   				    18.0
         				18.1
         				18.2
         				18.3
         				18.4
         				18.5
         				18.6
         				18.7
         				18.8
         				18.9
19   				    19.0
         				19.1
         				19.2
         				19.3
         				19.4
         				19.5
         				19.6
         				19.7
         				19.8
         				19.9
20   				    20.0
         				20.1
         				20.2
         				20.3
         				20.4
         				20.5
         				20.6
         				20.7
         				20.8
         				20.9
21   				    21.0
         				21.1
         				21.2
         				21.3
         				21.4
         				21.5
         				21.6
         				21.7
         				21.8
         				21.9
22   				    22.0
         				22.1
         				22.2
         				22.3
         				22.4
         				22.5
         				22.6
         				22.7
         				22.8
         				22.9
23   				    23.0
         				23.1
         				23.2
         				23.3
         				23.4
         				23.5
         				23.6
         				23.7
         				23.8
         				23.9
24   				    24.0
         				24.1
         				24.2
         				24.3
         				24.4
         				24.5
         				24.6
         				24.7
         				24.8
         				24.9
25   				    25.0
         				25.1
         				25.2
         				25.3
         				25.4
         				25.5
         				25.6
         				25.7
         				25.8
         				25.9
26   				    26.0
         				26.1
         				26.2
         				26.3
         				26.4
         				26.5
         				26.6
         				26.7
         				26.8
         				26.9
27   				    27.0
         				27.1
         				27.2
         				27.3
         				27.4
         				27.5
         				27.6
         				27.7
         				27.8
         				27.9
28   				    28.0
         				28.1
         				28.2
         				28.3
         				28.4
         				28.5
         				28.6
         				28.7
         				28.8
         				28.9
29   				    29.0
         				29.1
         				29.2
         				29.3
         				29.4
         				29.5
         				29.6
         				29.7
         				29.8
         				29.9
30   				    30.0
         				30.1
         				30.2
         				30.3
         				30.4
         				30.5
         				30.6
         				30.7
         				30.8
         				30.9
31   				    31.0
         				31.1
         				31.2
         				31.3
         				31.4
         				31.5
         				31.6
         				31.7
         				31.8
         				31.9
32   				    32.0
         				32.1
         				32.2
         				32.3
         				32.4
         				32.5
         				32.6
         				32.7
         				32.8
         				32.9
33   				    33.0
         				33.1
         				33.2
         				33.3
         				33.4
         				33.5
         				33.6
         				33.7
         				33.8
         				33.9
34   				    34.0
         				34.1
         				34.2
         				34.3
         				34.4
         				34.5
         				34.6
         				34.7
         				34.8
         				34.9
35   				    35.0
         				35.1
         				35.2
         				35.3
         				35.4
         				35.5
         				35.6
         				35.7
         				35.8
         				35.9
36   				    36.0
         				36.1
         				36.2
         				36.3
         				36.4
         				36.5
         				36.6
         				36.7
         				36.8
         				36.9
37   				    37.0
         				37.1
         				37.2
         				37.3
         				37.4
         				37.5
         				37.6
         				37.7
         				37.8
         				37.9
38   				    38.0
         				38.1
         				38.2
         				38.3
         				38.4
         				38.5
         				38.6
         				38.7
         				38.8
         				38.9
39   				    39.0
         				39.1
         				39.2
         				39.3
         				39.4
         				39.5
         				39.6
         				39.7
         				39.8
         				39.9
40   				    40.0
         				40.1
         				40.2
         				40.3
         				40.4
         				40.5
         				40.6
         				40.7
         				40.8
         				40.9
41   				    41.0
         				41.1
         				41.2
         				41.3
         				41.4
         				41.5
         				41.6
         				41.7
         				41.8
         				41.9
42   				    42.0
         				42.1
         				42.2
         				42.3
         				42.4
         				42.5
         				42.6
         				42.7
         				42.8
         				42.9
43   				    43.0
         				43.1
         				43.2
         				43.3
         				43.4
         				43.5
         				43.6
         				43.7
         				43.8
         				43.9
44   				    44.0
         				44.1
         				44.2
         				44.3
         				44.4
         				44.5
         				44.6
         				44.7
         				44.8
         				44.9
45   				    45.0
         				45.1
         				45.2
         				45.3
         				45.4
         				45.5
         				45.6
         				45.7
         				45.8
         				45.9
46   				    46.0
         				46.1
         				46.2
         				46.3
         				46.4
         				46.5
         				46.6
         				46.7
         				46.8
         				46.9
47   				    47.0
         				47.1
         				47.2
         				47.3
         				47.4
         				47.5
         				47.6
         				47.7
         				47.8
         				47.9
48   				    48.0
         				48.1
         				48.2
         				48.3
         				48.4
         				48.5
         				48.6
         				48.7
         				48.8
         				48.9
49   				    49.0
         				49.1
         				49.2
         				49.3
         				49.4
         				49.5
         				49.6
         				49.7
         				49.8
         				49.9
50   				    50.0
         				50.1
         				50.2
         				50.3
         				50.4
         				50.5
         				50.6
         				50.7
         				50.8
         				50.9
51   				    51.0
         				51.1
         				51.2
         				51.3
         				51.4
         				51.5
         				51.6
         				51.7
         				51.8
         				51.9
52   				    52.0
         				52.1
         				52.2
         				52.3
         				52.4
         				52.5
         				52.6
         				52.7
         				52.8
         				52.9
53   				    53.0
         				53.1
         				53.2
         				53.3
         				53.4
         				53.5
         				53.6
         				53.7
         				53.8
         				53.9
54   				    54.0
         				54.1
         				54.2
         				54.3
         				54.4
         				54.5
         				54.6
         				54.7
         				54.8
         				54.9
55   				    55.0
         				55.1
         				55.2
         				55.3
         				55.4
         				55.5
         				55.6
         				55.7
         				55.8
         				55.9
56   				    56.0
         				56.1
         				56.2
         				56.3
         				56.4
         				56.5
         				56.6
         				56.7
         				56.8
         				56.9
57   				    57.0
         				57.1
         				57.2
         				57.3
         				57.4
         				57.5
         				57.6
         				57.7
         				57.8
         				57.9
58   				    58.0
         				58.1
         				58.2
         				58.3
         				58.4
         				58.5
         				58.6
         				58.7
         				58.8
         				58.9
59   				    59.0
         				59.1
         				59.2
         				59.3
         				59.4
         				59.5
         				59.6
         				59.7
         				59.8
         				59.9
60   				    60.0
         				60.1
         				60.2
         				60.3
         				60.4
         				60.5
         				60.6
         				60.7
         				60.8
         				60.9
61   				    61.0
         				61.1
         				61.2
         				61.3
         				61.4
         				61.5
         				61.6
         				61.7
         				61.8
         				61.9
62   				    62.0
         				62.1
         				62.2
         				62.3
         				62.4
         				62.5
         				62.6
         				62.7
         				62.8
         				62.9
63   				    63.0
         				63.1
         				63.2
         				63.3
         				63.4
         				63.5
         				63.6
         				63.7
         				63.8
         				63.9
64   				    64.0
         				64.1
         				64.2
         				64.3
         				64.4
         				64.5
         				64.6
         				64.7
         				64.8
         				64.9
65   				    65.0
         				65.1
         				65.2
         				65.3
         				65.4
         				65.5
         				65.6
         				65.7
         				65.8
         				65.9
66   				    66.0
         				66.1
         				66.2
         				66.3
         				66.4
         				66.5
         				66.6
         				66.7
         				66.8
         				66.9
67   				    67.0
         				67.1
         				67.2
         				67.3
         				67.4
         				67.5
         				67.6
         				67.7
         				67.8
         				67.9
68   				    68.0
         				68.1
         				68.2
         				68.3
         				68.4
         				68.5
         				68.6
         				68.7
         				68.8
         				68.9
69   				    69.0

```

## Question 2
Instructions: Write a program that reads in a string from the user, have the program print one character at a time.

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
Instructions: Write a program that reads input from a given file (ICS 4U Assignment 1.1.txt, same as before). Read the file into your program. If you haven’t done it for the last assignment, create a new file to store your file input code. Create a function that takes file input. The parameter for this function will be a string (The file name). This function will return a string with the contents of the file. Have the program count and display how many vowels exist. Have the program count and display how many consonants exist. Your program must not count white space. Remember y is only a vowel if it is at the end of a word. I am expecting you to have a proper check for this. You may also want to be sure your reader is making sure there’s a space after each new line, or ensure there are new lines in your string. Why? Because this can happen “dayToseek”. There is a vowel in ‘day’ but because there’s nothing separating the ‘To’ it won’t count it.

Source Code:
```
// Question 4 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;

class Main{
public static String fileReader(String nameOfFile)
{
  Scanner input = null;
  String file = "";

  try
  {
    input = new Scanner(new File(nameOfFile));
  }
  catch (FileNotFoundException e)
  {
    System.out.println("There was an error with the file.");
  }
  while(input.hasNext())
  {
    file += input.nextLine();
    file += " ";
  }
  return file;
}

public static void main(String[] args)
{
  String punctuation=".,;! ";
  String allVowels ="aeiouAEIOU";
  int vowels = 0;
  int consonants = 0;

  String file = fileReader(" ICS4UASsignment11.txt");
  for (int i = 0; i < file.length(); i++)
  {
    char charFile = file.charAt(i);
    if (character.isLetter(CharFile))
    {
      if(allVowels.indexOf(file.charAt(i)) != -1)
      {
        vowels++;
      }
      else if((charFile == "y") && (punctuation.indexOf(file.charAT(i+1)) != -1))
      {
        vowels++;
      }
      else
      {
        consonants++;
      }
    }
  }
  System.out.println("The amount of vowels in your file: " + vowels);
  System.out.println("The amount of consonants in your program: " + consonants);
}
}

```

Sample Output:
```
The amount of vowels in your file: 425
The amount of consonants in your file: 757
```

## Question 5
Instructions: Write a program that reads input from a given file (ICS 4U Assignment 1.2.txt). Read the file into your program. Have the program store each word inside of an array. Once you have this completed, sort the array using a bubble sort (You might want to write this bubble sort in a separate file and in a function for reuse). Once sorted have the program prompt the user repeatedly to enter a phrase. Ensure proper error checking (Use the function you made in question 2). Have the program output “Found” if the word is in the array or “Not Found” if the word is not in the array. Exit when the user enters -1. Make sure your search is case sensitive.

Source Code:
```
// Question 5 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

import java.io.File;
import java.io.FileNotFoundException;
import java.util.Scanner;
import java.util.Arrays;

class Main
{
  public static void main(String[] args)
  {
    int counter = 0;
    Scanner input = null;
    String [] fileWords = new String [460];

    try
    {
      input = new Scanner(new File("ICS4UAssignment12.txt"));
    }
    catch (FileNotFoundException e)
    {
      System.out.println("There was an error with this file.");
      e.printStackTrace();
    }
    while (input.hasNextLine())
    {
      Scanner s2 = new Scanner(input.nextLine());
      while(s2.hasNext())
      {
        String word = s2.next();
        fileWords[counter] = word;
        counter ++;
      }
    }
    String punctuation = ".,;! ";
    int newCounter = 0;
    for(int i = 0; i < fileWords.length; i++)
    {
      if (punctuation.contains(fileWords[i]))
      {
        fileWords[i] = null;
      }
      else
      {
        newCounter++;
      }
    }
    String [] newWords = new String[newCounter];
    int wordCounter = 0;
    for(int i = 0; i<counter; i++)
    {
      if (fileWords[i] != null)
      {
        newWords[wordCounter] = fileWords[i];
        wordCounter ++;
      }
    }
    Arrays.sort(newWords);
    Scanner scan = new Scanner(System.in);
    String exit = "-1";

    while(true)
    {
      System.out.println("Please enter your word: ")
      String userInput = scan.nextLine();
      int userInputFound = 0;

      if(userInput.compareTo(exit) == 0)
      {
        break;
      }
      else
      {
        for(int i = 0; i<wordCounter; i++)
        {
          if(newWords[i].compareTo(userInput) == 0)
          {
            userInputFound++;
          }
        }
      }
      System.out.println("The word " + userInput+" is found "+ userInputFound + "times in the poem.");
    }
    System.out.println("While loop broken.")
  }
}
```

Sample Output:
```
Please enter your phrase
and
Your phrase is in the poem 12 times
Please enter your phrase
-1
```

## Question 6
Instructions: Write a program, that contains graphics and is a slot machine (Research slot machines if you don’t know what they are)

Source Code:
```
// Question 6 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

// Import packages for graphics, and random number generation
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.Random;

class Main
{
  public static void main(String[] args)
  {
    // Window setup / title bar
    JFrame window = new Jframe("Slot Machine");
    window.setSize(640,480);
    window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    //Call upon png images used in the game.
    ImageIcon bar = new ImageIcon("Bar.PNG");
    ImageIcon cherry = new ImageIcon("Cherry.PNG");
    ImageIcon seven = new ImageIcon("Seven.PNG")

    //Create spaces where icons will sit
    JLabel images[][] = new JLabel[3][3];

    // Starting pos of images before user plays the game
    // Row 1
    images[0][0] = new JLabel(bar);
    images[0][1] = new JLabel(bar);
    images[0][2] = new JLabel(bar);

    //Row 2
    images[1][0] = new JLabel(cherry);
    images[1][1] = new JLabel(cherry);
    images[1][2] = new JLabel(cherry);

    //Row 3
    images[2][0] = new JLabel(seven);
    images[2][1] = new JLabel(seven);
    images[2][2] = new JLabel(seven);

    JPanel panel = new JPanel(new GridBagLayout());
    GridBagConstraints constraints = new GridBagConstraints();

    //Button panel
    Jpanel buttonPanel = new JPanel();
    JButton button = new JButton("Spin");

    // This section is for what happens after the spin button is pressed
    button.addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent e)
      {
        //Create array for images
        ImageIcon [] imageList = (bar, cherry, seven);
        Random rand = new Random();
        // Create upperbound of 3, for the 3 images
        int upperBound = 3;

        //Every press of the spin button, change images at random
        //Row 1
        images[0][0].setIcon(imageList[rand.nextInt(upperBound)]);
        images[0][1].setIcon(imageList[rand.nextInt(upperBound)]);
        images[0][2].setIcon(imageList[rand.nextInt(upperBound)]);
        //Row 2
        images[1][0].setIcon(imageList[rand.nextInt(upperBound)]);
        images[1][1].setIcon(imageList[rand.nextInt(upperBound)]);
        images[1][2].setIcon(imageList[rand.nextInt(upperBound)]);
        //Row 3
        images[2][0].setIcon(imageList[rand.nextInt(upperBound)]);
        images[2][1].setIcon(imageList[rand.nextInt(upperBound)]);
        images[2][2].setIcon(imageList[rand.nextInt(upperBound)]);

        //Conditions for which the user will win the game (3 in a row)
        if(images[0][0].getIcon().equals(images[0][1].getIcon() && images[0][0].getIcon().equals(images[1][2].getIcon())))
        {
          //Print win message
          JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        // Horziontal win at y=1
        else if(images[1][0].getIcon()equals(images[1][1].getIcon()) && images[1][0].getIcon().equals(images[1][2].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        // Horizontal win at y=2
        else if(images[2][0].getIcon()equals(images[2][1].getIcon()) && images[2][0].getIcon().equals(images[2][2].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        // Vertical win at x=0
        else if(images[0][0].getIcon()equals(images[1][0].getIcon()) && images[0][0].getIcon().equals(images[2][0].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        // Vertical win at x=1
        else if(images[0][1].getIcon()equals(images[1][1].getIcon()) && images[0][1].getIcon().equals(images[2][1].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        //Vertical win at x=2
        else if(images[0][2].getIcon()equals(images[1][2].getIcon()) && images[0][2].getIcon().equals(images[2][2].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        // For diagonal win from top left to bottom right
        else if(images[0][0].getIcon()equals(images[1][1].getIcon()) && images[0][0].getIcon().equals(images[2][2].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        //For diagonal win from top right to bottom left
        else if(images[0][2].getIcon()equals(images[1][1].getIcon()) && images[0][2].getIcon().equals(images[2][0].getIcon())))
        {
        //Print winning message
        JOptionPane.showMessageDialog(null, "YOU WIN!");
        }
        //If user loses
        else
        {
          //Print loss message
          JOptionPane.showMessageDialog(null, "YOU LOSE!");
        }
      }
    }};
    //Insets are padding, new insets (top, left, bot, right), gridx and gridy are columns and rows
    buttonPanel.add(button);

    //Row 1 Insert
    constraints.gridx = 0;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[0][0],constraints);

    constraints.gridx = 1;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[0][1],constraints);

    constraints.gridx = 2;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[0][2],constraints);

    //Row 2 Insert
    constraints.gridx = 0;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[1][0],constraints);

    constraints.gridx = 1;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[1][1],constraints);

    constraints.gridx = 2;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[1][2],constraints);

    //Row 3 Insert
    constraints.gridx = 0;
    constraints.gridy = 2;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[2][0],constraints);

    constraints.gridx = 1;
    constraints.gridy = 2;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[2][1],constraints);

    constraints.gridx = 2;
    constraints.gridy = 2;
    constraints.insets = new Insets(0,0,10,10)
    panel.add(images[2][2],constraints);

    // Make everything visible
    window.add(buttonPanel, BorderLayout.NORTH);
    window.add(panel);
    window.setVisible(true);
  }
}

```

Sample Output:

![yes2](https://user-images.githubusercontent.com/35504711/137824118-5756048d-f74d-46af-8f4a-8b2ee61303e0.png)

## Question 7
Instructions: Write a program, that simulates a vending machine. Have your program read input for the product and price from a file. You can either set this up and parse it however you like, or if you’re courageous, store the data in either an XML or JSON file (These data types are important in industry). Once you have the data parsed and stored properly (Arrays) create a GUI frontend to display the data. For the GUI have an input Text Field to enter money. Have each product you imported represented by a button. The program has an output label that says “Here is your product” product being the name from text file and “Here’s your change $$$$”, $$$$ will be the answer to the number from the Text Field - price from the product selected. If the money entered is too little output “You didn’t put enough money”. Have your popup say “You didn’t put any money” if the have a character in the text box. You can hardcode the amount of buttons/product or you can try to figure out how to make it dynamic with the buttons going in a 3 in a row grid (hint: you can play around with JPanels, layouts, and .add()).

Source Code:
```
// Question 7 - ICS4U1 Review Assignment
// Brandon Wong-Dearing
// Teacher: Mr. Naccarto

import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.Scanner;
import java.io.File;
import java.io.FileNotFoundException;

class Main
{
  public static void main(String[] args)
  {
    Scanner soda = null;
    String coke;
    String cokePrice;
    String pepsi;
    String pepsiPrice;
    String nestea;
    String nesteaPrice;
    String gassosa;
    String gassosaPrice;
    String canadaDry;
    String canadaDryPrice;
    String sprite;
    String spritePrice;

    try
    {
      soda = new Scanner(new File("Prices.txt"));
    }
    catch (FileNotFoundException e)
    {
      System.out.println("There was an error with the file.");
      e.printStackTrace();
    }
    coke = soda.nextLine();
    cokePrice = soda.nextLine();
    pepsi = soda.nextLine();
    pepsiPrice = soda.nextLine();
    nestea = soda.nextLine();
    nesteaPrice = soda.nextLine();
    gassosa = soda.nextLine();
    gassosaPrice = soda.nextLine();
    canadaDry = soda.nextLine();
    canadaDryPrice = soda.nextLine();
    sprite = soda.nextLine();
    spritePrice = soda.nextLine();

    // Window setup
    JFrame window = newJFrame("Vending Machine V1.0");
    window.setSize(640,480);
    window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    JPanel panel = new JPanel(new GridBagLayout());
    GridBagConstraints constraints = new GridBagConstraints();

    JButton sodas[][] = new JButton[2][3];

    sodas[0][0] = new JButton(coke + " $" + cokePrice);
    sodas[0][1] = new JButton(pepsi + " $" + pepsiPrice);
    sodas[0][2] = new JButton(nestea + " $" + nesteaPrice);
    sodas[1][0] = new JButton(gassosa + " $" + gassosaPrice);
    sodas[1][1] = new JButton(canadaDry + " $" + canadaDryPrice);
    sodas[1][2] = new JButton(sprite + " $" + spritePrice);

    JTextField userInput = new JTextField("Enter money deposited: ");
    panel.add(userInput);

    sodas[0][0].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(cokePrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ coke + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    sodas[0][1].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(pepsiPrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ pepsi + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    sodas[0][2].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(nesteaPrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ nestea + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    sodas[1][0].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(gassosaPrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ gassosa + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    sodas[1][1].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(canadaDryPrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ canadaDry + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    sodas[1][2].addActionListener(new ActionListener())
    {
      @Override
      public void actionPerformed(ActionEvent arg0)
      {
        try
        {
          String userInputString == userInput.getText();
          double userInputMoney = Double.parseDouble(userInputString);
          if(userInputMoney >= Double.parseDouble(cokePrice))
          {
            userInputMoney = userInputMoney-Double.parseDouble(spritePrice);
            userInputString = String.format("%.2f", userInputMoney);
            userInput.setText(userInputString);
            JOptionPane.showMessageDialog(null, "Here is your "+ sprite + ". Your change is $" + userInputString);
          }
          else
          {
            JOptionPane.showMessageDialog(null, "You are missing funds.");
          }
        }
        catch(Exception e)
        {
          JOptionPane.showMessageDialog(null, "You didn't deposit any money");
        }
      }
    }};

    //Row 1
    constraints.gridx = 0;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[0][0],constraints);

    constraints.gridx = 1;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[0][1],constraints);

    constraints.gridx = 2;
    constraints.gridy = 0;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[0][2],constraints);

    //Row 2
    constraints.gridx = 0;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[1][0],constraints);

    constraints.gridx = 1;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[1][1],constraints);

    constraints.gridx = 2;
    constraints.gridy = 1;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(sodas[1][2],constraints);

    //Row 3 JTextField / User Input
    constraints.gridx = 1;
    constraints.gridy = 2;
    constraints.insets = new Insets(0,0,10,10);
    panel.add(userInput,constraints);

    //Make everything visible
    window.add(panel);
    window.setVisible(true);
  }
}
```

Sample Output:

![image](https://user-images.githubusercontent.com/35504711/137825436-b5693ffd-2416-4636-b770-d81f11004015.png)
