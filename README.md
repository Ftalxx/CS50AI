# Degrees Program
Welcome to my attempt to solve and navigate through CS50's Introduction to Artificial Intelligence with Python projects. This one is from Lesson 0.

## Project Purpose
The goal of this project is to determine the number of "degrees of separation" between two actors, similar to the "Six Degrees of Kevin Bacon" game. This involves finding the shortest path between any two actors by identifying the sequence of movies connecting them.

## Problem Description
In the Hollywood film industry, any actor can be connected to another within six steps, where each step involves a movie that two actors both starred in. This project frames the problem as a search problem and aims to find the shortest path between two actors by leveraging the connections made through their co-starring in films.

## Technologies Used
- Python 3.12: The primary programming language used for the project.
- CSV Files: Data format used to store information about actors, movies, and their relationships.

## Getting Started
- Download the Distribution Code
    Download from: Degrees Project Distribution
    Unzip the downloaded file.

- Understand the Data Files
    people.csv: Contains a unique ID for each person, their name, and birth year.
    movies.csv: Contains a unique ID for each movie, its title, and the year it was released.
    stars.csv: Establishes the relationship between people and movies, listing which actors starred in which films.

## Running the Project

- Load the Data
    The load_data function reads the CSV files and loads the data into memory, creating dictionaries for people, movies, and names.

- Prompt for Actor Names
    The main function will prompt you to enter two actor names. The person_id_for_name function retrieves the corresponding IDs, handling cases where multiple actors have the same name.

- Find the Shortest Path
    The shortest_path function uses breadth-first search to find the shortest path between the two actors based on their movie connections. It returns a list of (movie_id, person_id) pairs representing the path.

- Run the Program
    # $ python degrees.py large
    Enter the names of the actors when prompted. The program will output the number of degrees of separation and the sequence of movies connecting them.
  
## Example Usage

# $ python degrees.py large
# Loading data...
# Data loaded.
# Name: Emma Watson
# Name: Jennifer Lawrence
# 3 degrees of separation.
# 1: Emma Watson and Brendan Gleeson starred in Harry Potter and the Order of the Phoenix
# 2: Brendan Gleeson and Michael Fassbender starred in Trespass Against Us
# 3: Michael Fassbender and Jennifer Lawrence starred in X-Men: First Class

## Implementation Details
- Data Structures: Dictionaries for names, people, and movies.
- Function to Complete: shortest_path
    Should return the shortest path as a list of tuples.
    Can call neighbors_for_person to get co-starring actors.
    Should check for the goal when nodes are added to the frontier for efficiency.

## Hints
- Check for the goal when adding nodes to the frontier to improve search efficiency.
- Use and adapt the provided Node, StackFrontier, and QueueFrontier implementations from util.py.
