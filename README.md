# Quiz Game

Need to create a program that will read in a quiz provided via a CSV file (or other formats) and will then give the quiz to a user keeping track of how many questions they get right and how many they get incorrect.

Original task: https://courses.calhoun.io/lessons/les_goph_01

## Quiz rule

Regardless of whether the answer is correct or wrong the next question should be asked immediately afterwards.

At the end of the quiz the program should output the total number of questions correct and how many questions there were in total. Questions given invalid answers are considered incorrect.

## CSV file format

The CSV file should default to problems.csv (example shown below), but the user should be able to customize the filename via a flag.

The CSV file will be in a format like below, where the first column is a question and the second column in the same row is the answer to that question.

```
5+5;10
7+3;10
1+1;2
8+3;11
1+2;3
8+6;14
3+1;4
1+4;5
5+1;6
2+3;5
3+3;6
2+4;6
5+2;7
```

## Run the game

It is assumed that you already have Go sources. If not, then you can look at the installation on the official website https://go.dev/dl/.

Before starting the game, you need to define the rules in a certain format.
By default, the rules are set in csv format in the file /assets/problems.csv.

To launch the game, run the following commands in **cmd** directory:

To build:
```
go build -o quiz .
```

To run:
```
./quiz
```

To change problems file filepath:
```
./quiz -filepath="new path"
```

To get help:
```
./quiz --help
```