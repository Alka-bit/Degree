# Degree

CS50’s Introduction to Artificial Intelligence with Python : <a href="https://cs50.harvard.edu/ai/2020/projects/0/degrees/#:~:text=CS50%E2%80%99sIntroduction%20to%20Artificial%20Intelligence%20with%20Python">Project 0</a>

Download the distribution code from <a href="https://cdn.cs50.net/ai/2020/x/projects/0/degrees.zip">here</a> and unzip it.

# Background of the Project

According to the <a href="https://en.wikipedia.org/wiki/Six_Degrees_of_Kevin_Bacon">Six Degrees of Kevin Bacon game</a>, anyone in the Hollywood film industry can be connected to Kevin Bacon within six steps, where each step consists of finding a film that two actors both starred in.

In this problem, we’re interested in finding the shortest path between any two actors by choosing a sequence of movies that connects them. For example, the shortest path between Jennifer Lawrence and Tom Hanks is 2: Jennifer Lawrence is connected to Kevin Bacon by both starring in “X-Men: First Class,” and Kevin Bacon is connected to Tom Hanks by both starring in “Apollo 13.”

# Problem Statement

Our states are people. Our actions are movies, which take us from one actor to another (it’s true that a movie could take us to multiple different actors, but that’s okay for this problem). Our initial state and goal state are defined by the two people we’re trying to connect. By using breadth-first search, we can find the shortest path from one actor to another.

# Specification

Complete the implementation of the shortest_path function such that it returns the shortest path from the person with id source to the person with the id target.

Assuming there is a path from the source to the target, your function should return a list, where each list item is the next (movie_id, person_id) pair in the path from the source to the target. Each pair should be a tuple of two ints.
For example, if the return value of shortest_path were [(1, 2), (3, 4)], that would mean that the source starred in movie 1 with person 2, person 2 starred in movie 3 with person 4, and person 4 is the target.
If there are multiple paths of minimum length from the source to the target, your function can return any of them.
If there is no possible path between two actors, your function should return None.
You may call the neighbors_for_person function, which accepts a person’s id as input, and returns a set of (movie_id, person_id) pairs for all people who starred in a movie with a given person.
You should not modify anything else in the file other than the shortest_path function, though you may write additional functions and/or import other Python standard library modules.

