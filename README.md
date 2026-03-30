This project is called the Smart Campus Navigation System. It is a web-based system that helps users find their way around the USANT campus. The user selects a starting building and a destination building, then the system will either:

Find the shortest path between them, or
Check if the two buildings are connected

The system also shows a visual map, highlights the path, and displays the total distance.

💻 How the System Works

The system is built using:

HTML → structure of the webpage
CSS → design and layout (map, colors, animations)
JavaScript → logic and algorithms

The campus is represented as a graph:

Buildings = nodes (vertices)
Roads = edges (connections)

Each building has coordinates, and distances are computed automatically.

📊 Data Structures Used
Locations
Stores all buildings with their positions on the map

Example:

"Library": {x:30, y:20}
Connections
Defines which buildings are connected

Example:

["Library", "CIBM"]
Graph (Adjacency List)
Stores neighbors and distances
Used by the algorithms
📏 Distance Calculation

The system uses the Euclidean Distance Formula to calculate distance between buildings:

Then it converts it into kilometers (2 km to 20 km range) for realism.
🔍 Algorithms Used
✅ 1. Dijkstra’s Algorithm (Shortest Path)

This algorithm finds the shortest route between two buildings.

Simple Explanation (Student Style):

Start from the selected building
Check all connected buildings
Always choose the shortest distance available
Repeat until reaching the destination

👉 It also keeps track of the path so it can be displayed.

Example Output:

✨ Path: Registrar → Library → CIBM → MIS → SHS → Events
📏 Distance: 15 km
🔄 2. Breadth-First Search (BFS) – Connectivity

This algorithm checks if two buildings are connected at all, even if it's not the shortest.

Simple Explanation:

Start from one building
Visit all nearby buildings
Continue until:
Destination is found → ✅ Connected
No more buildings → ❌ Not Connected

Example Output:

✅ Connected
🗺️ Map Visualization

The system visually shows:

🟢 Start building
🔴 Destination
🟡 Path buildings
📏 Lines with distance labels

This makes it easier for users to understand the route.

🧪 Sample Input and Output
Example 1: Shortest Path

Input:

Start: Registrar
End: Events

Output:

✨ Path: Registrar → Library → CIBM → MIS → SHS → Events
📏 Distance: 15 km
Example 2: Connectivity Check

Input:

Start: President
End: Research

Output:

✅ Connected

