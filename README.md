# Degrees
### Harvard CS50's Introduction to Artificial Intelligence with Python (Project 0)

This project calculates how many "degrees of separation" apart two actors are.

## Problem Description
In this problem, we’re interested in finding the *shortest path* between any two actors by choosing a sequence of movies that connects them. For example, the shortest path between Jennifer Lawrence and Tom Hanks is 2: Jennifer Lawrence is connected to Kevin Bacon by both starring in “X-Men: First Class,” and Kevin Bacon is connected to Tom Hanks by both starring in “Apollo 13.”

## Solution
We create a directed graph and perform *Breadth-first Search* to find the optimal (shortest) path between any two actors.

`shortest_path(source, targest)` function takes two arguments: `source` and `target`. It then performs **BFS**, starting from `source` as root node and stopping when the `target` node is found. If there exists no connection, this function returns `None`.<br>
Finally, if there exists a connection, it is displayed in a numbered list stating which two actors worked in which movie.

## Example
**Input:**
```python
Name: Jennifer Lawrence
Name: Emma Watson
```
**Output:**
```python
3 degrees of separation.
1: Jennifer Lawrence and Charlotte Rampling starred in Red Sparrow
2: Charlotte Rampling and Michael Gambon starred in Paris by Night
3: Michael Gambon and Emma Watson starred in Harry Potter and the Deathly Hallows: Part 2
```