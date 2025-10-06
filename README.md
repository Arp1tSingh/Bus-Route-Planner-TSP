College Bus Route Planner (TSP Solver)
Overview

The College Bus Route Planner is a console-based C program that calculates the optimal bus route for a set of college stops using the Traveling Salesperson Problem (TSP) algorithms. It supports exact and heuristic solutions, dynamic stop management, and file-based configuration.

The program allows users to:

Display all bus stops and the distance matrix.

Calculate shortest bus routes using:

Brute-Force (Exact)

Greedy / Nearest Neighbor (Heuristic)

Branch & Bound (Exact - Optimized)

Dynamically add new stops and modify distances.

Save and load configurations to/from a file.

Compare exact and heuristic algorithms.

Features

Algorithm Options

Brute-Force: Computes exact solution (slow for >10 stops).

Greedy / Nearest Neighbor: Fast heuristic for approximate routes.

Branch & Bound: Optimized exact solution with pruning.

Dynamic Stop Management

Add new stops with custom distances.

Modify existing distances.

Automatically recalculate optimal routes after updates.

Configuration Management

Save current stops and distances to bus_route_config.txt.

Load previously saved configuration.

User-Friendly Interface

Menu-driven console UI.

Robust input validation using fgets() and strtol().

Installation

Make sure you have a C compiler (GCC) installed.

Download the source code main.c.

Compile the program:

gcc main.c -o bus_planner


Run the program:

./bus_planner

Usage

The program runs in a menu-driven interface. Sample workflow:

Load Configuration (optional)

Load previous configuration? (1=Yes, 0=No): 0


Loads default stops if no saved configuration exists.

Main Menu Options

1. Display All Bus Stops
2. Display Distance Matrix
3. Find Shortest Route (Choose Algorithm)
4. Handle Added Stop (Dynamic Route Update)
5. Compare Exact vs Heuristic Solutions
6. Add New Bus Stop
7. Modify Distance Between Stops
8. File I/O (Save/Load Configuration)
9. Exit


Adding a Stop

Enter stop name.

Enter distances to all existing stops in order.

Selecting TSP Algorithm

Choose between Brute-Force, Greedy, or Branch & Bound.

The program will compute and display the optimal route with total distance.

File I/O

Save or load configurations easily.

View configuration info without modifying.

Sample Output
 OPTIMAL BUS ROUTE:
  Stop 1: Bus Depot (Start)
     ↓ (Distance: 5 units)
  Stop 2: Main Gate
     ↓ (Distance: 8 units)
  Stop 3: Library
     ↓ (Distance: 6 units)
  Stop 4: Hostel Block A
     ↓ (Distance: 11 units)
  Stop 5: Cafeteria
     ↓ (Distance: 12 units)
  Stop 6: Sports Complex
     ↓ (Distance: 20 units)
  Stop 7: Bus Depot (Start)

📏 TOTAL DISTANCE: 62 units (6.2 km)

File Structure

main.c: Main program source code.

bus_route_config.txt: Stores user-defined stops and distances (created at runtime).

Algorithm Details
Brute-Force TSP

Generates all permutations of stops.

Guarantees exact solution but computationally expensive.

Greedy / Nearest Neighbor

Starts at the depot, visits nearest unvisited stop iteratively.

Fast, approximate solution.

Branch & Bound

Uses node bounds and pruning to optimize search.

Exact solution with reduced computational time compared to brute-force.

Notes

Maximum stops allowed: 20.

Distance matrix is symmetric.

Robust input ensures the program does not crash on invalid input.

Branch & Bound and Brute-Force may take long for >10 stops.

Author

Arpit Singh

License

This project is open-source and free to use for educational purposes.
