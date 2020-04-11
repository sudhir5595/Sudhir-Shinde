# Intel Assignment
The problem is to Find identically-colored connected components in a triangle mesh with Open3D (The codes and other files has been added in the "Open3D/Document" folder).
Note :- All codes are executed and tested on Ubuntu 16.04

# Algorithm

To find the identically-colored connected components following algorithm is used:

* Build the graph from the triangle connectivity and the vertices. The vertices will be taken as nodes and connectivity of the triangle is edge of the graph
* Apply the Breadth First Search (BFS) algorithm to travel from the graph
* Maintain the visited array of nodes. If the node is not visited and the color of that node is same as source node then that nodes are connected and has same color.
* Travel the nodes which are not visited and store the result
* Sort the final vector

# Running Instruction

## For C++ Code
The Executive file has been added in the "Open3D/Document" folder (solution) to run the cpp code and generate results.txt file

	./solution <Name of the .ply model>
	
e.g:- ./solution test_mesh.ply	

## For python code
	
	python3 solution.py <Name of the .ply model>
  
  e.g:-  python3 solution.py test_mesh.ply
	
# Task

* Task 1 - the C++ function named IdenticallyColoredConnectedComponents has been added in the TriangleMesh.cpp file (Line no - 1334)
* Task 2 - The Python binding for the same has been added in the directory "Open3D/src/Python/open3d_pybind/geometry/TriangleMesh.cpp" (Line no - 212)
* Task 3 - solution.cpp file has been added in the directory "Open3D/examples/Cpp/solution.cpp"
* Task 4 - solution.py file has been added in the directory "Open3D/examples/Python/Basic/solution.py"
* Task 5 - Output of the result of the task "results.txt" file has been added in the "Open3D/Document/" folder
* Task 6 - C++ unit tests has been added in the TriangleMesh.cpp file in the directory "Open3D/src/UnitTest/Geometry/". Python unit test has been added in the file named "test_identically_colored_connected_components.py" file in the directory "Open3D/src/UnitTest/Python/"
