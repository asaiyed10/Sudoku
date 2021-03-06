# Sudokus and Graph

## Description

Sudoku is a logic-based,  combinatorial number-placement puzzle. The objective is to fill a 9×9 grid with digits so that
each column, each row, and each of the nine 3×3 sub-grids that compose the grid (also called "boxes", "blocks", "regions",
or "sub-squares") contains all of the digits from 1 to 9. The puzzle setter provides a partially completed grid, which typically 
has a unique solution.
Completed puzzles are always a type of Latin square with an additional constraint on the contents of individual regions.
For example, the same single integer may not appear twice in the same 9x9 playing board row or column or in any of the 
nine 3x3 subregions of the 9x9 playing board.

The puzzle was popularized in 1986 by the Japanese puzzle company Nikoli, under the name Sudoku, meaning single number.

Sudoku can be seen as a graph or 81 vertex, with edges connecting each cell with the ones in their row, column and 3x3 
cell. So if we see this problem as a graph coloring problem, we can use this kind of algorithms or to compose new sudoku
or to solve.

Althought this is not the most optimal solution for a sudoku, is a nice example where you can easy see the capabilities 
of graph coloring.

## What is graph coloring

Graph (Vertex or Edges) coloring is an assignment of labels traditionally called "colors" to elements of a graph 
subject to certain constraints. This problem can be seen as a contrain satisfaction problem, lets say for example you 
want to provide colors for the countries on a map, but that neightbours can never has the same color, or that you want to
choose the best time slot for an exam, or alocate registers in a computer. 

All this problems share the same denominator, we have objects with constrains that must be satisfied.

For a first overview on graph coloring methods you can take a look to:

+ http://en.wikipedia.org/wiki/Graph_coloring#Algorithms

+ http://www.math.tu-clausthal.de/Arbeitsgruppen/Diskrete-Optimierung/publications/2002/gca.pdf

+ http://scienceblogs.com/goodmath/2007/06/graph_coloring_algorithms_1.php

## Example

So on this exercice we got the definition of a sudoku and aim to get a solution using graph related algoritms. 
The file has the size of the sudoku as the first row, and a list of already assignated values with the form (row, column, value).

## Input

    9,9
    0,1,4
    0,3,6
    0,7,3
    0,8,2
    1,2,8
    1,4,2
    2,0,7
    2,3,8
    3,3,5

## Output

The sudoku matrix

    1 2 3 4 5 6 7 8 9
    2 3 ........... 8
    3 ............. 7
    4 ............. 6
    5 ............. 5
    6 ............. 4
    7 ............. 3
    8 ............. 2
    9 ............. 1
