# Assignment-1-Computus-solution

Download Here: [Assignment 1: Computus solution](https://jarviscodinghub.com/assignment/assignment-1-computus-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Introduction
People in Hong Kong enjoy Easter holiday every year, but do you know how the Easter Day is
determined? The calculation of Easter Day in the Christian calendar is known as Computus (Latin for
computation). In principle, Easter Day is the first Sunday after the 14th day of the lunar month (the
nominal full moon) that falls on or after 21 March (nominally the vernal equinox 春分 in Northern
Hemisphere). In this assignment, you will write a program to calculate the Easter Day for some given
years.
The following shows an algorithm to calculate the Easter Day for a particular ????. It is valid for all
Gregorian years. (Gregorian calendar is the Western calendar system which we are in use today. It
was a refinement in the 16th century to the previous system on the scheme of leap years.) At the end
of the algorithm, ????ℎ and ??? represent the Easter Day of the ????.
? = ???? mod 19
? = ⌊
????
100 ⌋
? = ???? mod 100
? = ⌊
?
4
⌋
? = ? mod 4
? = ⌊
? + 8
25 ⌋
? = ⌊
? − ? + 1
3
⌋
ℎ = (19? + ? − ? − ? + 15) mod 30
? = ⌊
?
4
⌋
? = ? mod 4
? = (32 + 2? + 2? − ℎ − ?) mod 7
? = ⌊
? + 11ℎ + 22?
451 ⌋
????ℎ = ⌊
ℎ + ? − 7? + 114
31 ⌋
??? = ((ℎ + ? − 7? + 114) mod 31) + 1
Note that ⌊?⌋ means the floor of ?, that is, the largest integer not greater than ?, and mod is the
modulo operation (e.g., 7 mod 3 = 1).
Example: ???? = 2015.
? = 2015 mod 19 = 1
? = ⌊
2015
100 ⌋ = 20

? = 2015 mod 100 = 15
? = ⌊
20
4
⌋ = 5
? = 20 mod 4 = 0
? = ⌊
20 + 8
25 ⌋ = 1
? = ⌊
20 − 1 + 1
3
⌋ = 6
ℎ = (19 × 1 + 20 − 5 − 6 + 15) mod 30 = 43 mod 30 = 13
? = ⌊
15
4
⌋ = 3
? = 15 mod 4 = 3
? = (32 + 2 × 0 + 2 × 3 − 13 − 3) mod 7 = 22 mod 7 = 1
? = ⌊
1 + 11 × 13 + 22 × 1
451 ⌋ = 0
????ℎ = ⌊
13 + 1 − 7 × 0 + 114
31 ⌋ = 4
??? = ((13 + 1 − 7 × 0 + 114) mod 31) + 1 = 5
Therefore, the Easter day in 2015 is 5 Apr 2015.
Program Specification
The program will obtain two years as user input. You can assume that the two input years are always
integers greater than 1582 (when the Gregorian calendar was first adopted) and no greater than
9999. The output is the date of the Easter Day of all years between the two input years (inclusively)
in ascending years, in the format dd/mm/yyyy. Note that the day and month are always two-digit,
while year is always 4-digit. In addition, you have to count the number of March and April Easter
Days respectively in the input year range. Note that it is still an acceptable input when the first input
year is larger than the second input year. (See the third sample run below.)
Program Output
The following shows some sample output of the program. The bold blue text is user input and the
other text is the program output. You can try the provided sample program for other input. Your
program output should be exactly the same as the sample program (i.e., same text, same symbols,
same letter case, same number of spaces, etc.). Otherwise, it will be considered as wrong, even if
you have computed the correct result.
Enter year range: 2010 2020↵
Easter Day in 2010 is 04/04/2010.
Easter Day in 2011 is 24/04/2011.
Easter Day in 2012 is 08/04/2012.
Easter Day in 2013 is 31/03/2013.
Easter Day in 2014 is 20/04/2014.
Easter Day in 2015 is 05/04/2015.
Easter Day in 2016 is 27/03/2016.
Easter Day in 2017 is 16/04/2017.

Easter Day in 2018 is 01/04/2018.
Easter Day in 2019 is 21/04/2019.
Easter Day in 2020 is 12/04/2020.
In March: 2
In April 9
Enter year range: 1583 1583↵
Easter Day in 1583 is 10/04/1583.
In March: 0
In April: 1
Enter year range: 2046 2040↵
Easter Day in 2040 is 01/04/2040.
Easter Day in 2041 is 21/04/2041.
Easter Day in 2042 is 06/04/2042.
Easter Day in 2043 is 29/03/2043.
Easter Day in 2044 is 17/04/2044.
Easter Day in 2045 is 09/04/2045.
Easter Day in 2046 is 25/03/2046.
In March: 2
In April: 5
Submission and Marking
 Your program file name should be computus.cpp. Submit the file in Blackboard
(https://elearn.cuhk.edu.hk/).
 Insert your name, student ID, and e-mail address as comments at the beginning of your source
file.
 You can submit your assignment multiple times. Only the latest submission counts.
 Your program should be free of compilation errors and warnings.
 Your program should include suitable comments as documentation.
 Plagiarism is strictly monitored and heavily punished if proven. Lending your work to others is
subjected to the same penalty as the copier.
