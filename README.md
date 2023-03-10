![football-match-reports](https://user-images.githubusercontent.com/44240533/222983859-5280b688-3489-4082-86b7-1814690865eb.svg)
# Football Match Reports

Welcome to Football Match Reports on Exercism's Java Track.
If you need help running the tests or submitting your code, check out `HELP.md`.
If you get stuck on the exercise, check out `HINTS.md`, but try and solve it without using those first :)

## Introduction

Like an _if/else_ statement, a `switch` statement allow you to change the flow of the program by conditionally executing code. The difference is that a `switch` statement can only compare the value of a primitive or string expression against pre-defined constant values.

Some keywords are usefull when using a switch statement.

- `switch` : this keyword allow you to declare the structure of the switch. It his follow by the expression or the variable that will make the result change.
- `case` : you will use this one to declare the differents possibilties for the result.
- `break` : the `break` keyword is very usefull in order to stop the execution of the switch at the end of the wanted flow. If you forget it, the program will continue and may lead to unexpected results.
- `default` : as it's name says use it as a default result when no other case matchs your expression's result.

At their simplest they test a primitive or string expression and make a decision based on its value. For example:

```java
String direction = getDirection();
switch (direction) {
    case "left":
        goLeft();
        break;
    case "right":
        goRight();
        break;
    default:
        //otherwise
        markTime();
        break;
}
```

## Instructions

You are developing a system to help the staff of a football/soccer club's web site report on matches. Data is received from a variety of sources and piped into a single stream after being cleaned up.

## 1. Output descriptions of the players based on their shirt number

The team only ever plays a 4-3-3 formation and has never agreed with the 1965 change to the rules allowing for substitutions, never mind enlarged squads.

The player descriptions are as follows:

```
1 -> "goalie"
2 -> "left back"
3 & 4 "center back"
5 -> "right back"
6, 7, & 8 -> "midfielder"
9 -> "left wing"
10 -> "striker"
11 -> "right wing"
```

Implement the static `FootballMatchReports.onField()` method to output a player description based on their shirt number.

```java
FootballMatchReports.onField(10);
// => "striker"
```

## 2. Raise an alert if an unknown shirt number is encountered

Modify the `FootballMatchReports.onField()` method to throw an `IllegalArgumentException` when a shirt number outside the range 1-11 is processed.

```java
FootballMatchReports.onField(13);
// => Throw IllegalArgumentException
```

## Source

### Created by

- @Azumix
