# Dijkstra

Computation of the Dijkstra minimum cost path. Based on Google Colab 

The program has two main parts:

## Part 1: 
Automagtic generation and visualization of Graph, including Nodes, Connections and Costs associated to each.

### Step 1
Define the number of nodes. The connections and costs are randomly generated
<p align="center">
  <img src="/images/GraphGen01.png" alt="Graph Initialization">
  <br>
  Graph initialization after indicating the number of nodes
</p>

###Step 2
The program will show the generated graph

<p align="center">
  <img src="/images/GraphGen02.png" alt="Graph Initialization" width="500">
  <br>
  Graph visualization, including nodes, connections and costs
</p>

And will request for the initial node

<p align="center">
  <img src="/images/GraphGen03.png" alt="Graph Initialization">
  <br>
  Selection of initial node
</p>

###Note: Users can also generate new graphs based on the JSON example provided at the fist part or use the automatic generator.

Example of JSON graph description
<pre><code>
network_data = {
  "nodes": ["A", "B", "C", "D", "E"],
  "edges": [
     {"source": "A", "destination": "B", "cost": 2},
    {"source": "A", "destination": "C", "cost": 4},
    {"source": "B", "destination": "C", "cost": 1},
    {"source": "B", "destination": "D", "cost": 7},
    {"source": "C", "destination": "E", "cost": 3},
    {"source": "D", "destination": "E", "cost": 1}
  ],
  "start_node": "A"
}
</code></pre>


### WARNING: The "Process Dijkstra" button is stil not working. Manual execution of the code block is required once the graph is defined.

## Part 2:
Computation of the Dijkstra minimum cost path. 

* At each step, the program shows the graph with the nodes and the table
<p align="center">
  <img src="/images/DJKStep0All.png" alt="Four steps during process">
  <br>
  Selection of initial node
</p>  

* At the end of the computation, it shows the resulting tables with the computation

<p align="center">
  <img src="/images/FinalTable.png" alt="Final results">
  <br>
  Selection of initial node
</p>  






