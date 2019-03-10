# How many the shortest ways are there? (Advanced)

Keywords: `Taxicab Geometry`, `Analytical Programming`, `Procedural Thinking`

## Overview

Prerequisite: `How many the shortest ways are there?`

Students will develop algorithmic thinking skills to move rabbits from one side to another side of the city. Students will then learn how many different ways exist to move in the shortest way. Delving deeper, students will learn the how many distinct paths are there, and understand the basics of `iteration` (commonly used as 	`for loop` in coding.)

## Purpose

In this course, students will develop logical thinking skills and understand a slight preview of discrete mathematics. This course does not require any computer equipment, so therefore students have no burden understanding the computer programming languages.

## Objectives

Students will be able to:

* Translate movements into a series of commands.
* Count the shortest ways.
* Understand many shortest ways are there, given with M*N size city.
* Understand the basics of "Counting"

## Teaching Guide

### Warm up (3 minutes)

#### Display

* Show students the picture of the city map, which students previously explored the shortest path.

|Rabbit|------|------|------|------|------|
|------|------|------|------|------|------|
|------|------|------|------|------|------|
|------|------|------|------|------|------|
|------|------|------|------|------|Carrot|

* Remind the rules. 
   * The rabbit wants to get the carrot.
   * The rabbit can move to any block on right, left, upside, downside of the current block.
   * How should the rabbit move?

### Discuss (3 minutes)

Try to find the shortest paths again! 
* How many "move right," "move downward" "move left" "move upward" are there?
* Is there any common properties?

#### After the students find some answers,

* Given that the city is 6 * 4 in size, is there any relationship with 5 "move right"s and 3 "move downward"s, what we have found?

> Teacher's guide

> If the carrot is on the opposite side of the city, the rabbit always need to travel (M-1) horizontally and (N-1) vertically, without moving back.

* If we rearrange the combination with same number of "move right"s and "move downward," what does the new combination mean?

> Teacher's guide

> It is another combination of the shortest path.

### Main Activity (4 minutes)

* How many distinct ways can we rearrange (M-1) horizontal moves and (N-1) vertical moves?
* There are M+N-2 moves in total.
* Let's say we pick one card within 8 cards. There are M+N-2 cases.
* Then, let's pick one more. We will have 7 choices.
* Repeat this until there is no more cards.
* There would be 8 * 7 * 6 * ... * 2 * 1 combinations.
* We denote this as `8!`, and read as `8 Factorial`, where Factorial means "Multiply n, n-1, n-2, ... , 2, 1."
* But in this case, we have 5 same cards, and 3 same cards (Horizontal moves and Vertical moves)
* Changing the first horizontal move and the third horizontal move would result in a same path. They are both the same horizontal move.
* So there are repeated cases where each horizontal moves and vertical moves are mixed with themselves.
* In total 8! of combinations, these 8! include 5! of horizontal move remixes, and 3! of vertiacal moves remixes.
* Then the final combination value would be <img src="https://latex.codecogs.com/gif.latex? 8! \over {5! \times 3!}"\> which is 56.

### Wrap up (5 minutes)
* If there is M * N size city, how many shortest path combination would there be?

> Teacher's guide

> Noting the previous example, we can guess that the combinations would be <img src="https://latex.codecogs.com/gif.latex? (M+N-2)! \over {(M-1)! \times (N-1)!}"\>