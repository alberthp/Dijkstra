# Dijkstra computation for a network of routers

## Description

Computation of the Dijkstra minimum cost paths between origin node and all rest of nodes in a non-directional (can be understood as bidirectional) network of routers. This program is designed to be an illustative method that shows minimum cost table and graph at each algorithm iteration.  

The network is defined as a graph where nodes represent the routers and the links the connections between them. Each link has an associated cost.

>[!NOTE]
>Developed as illustrative example for Networks topic in Universitat Pompeu Fabra (UPF).



The program has two separated parts:
1. Graph generation
2. Dijkstra min cost computation


## Program development
* Developed using Python 3
* Based on Google Colab 

## Graph generation

Graphs are defined using JSON file following this format:

> [!IMPORTANT]  
> The graph is non-directional, even JSON explicites "source" and "destination"

<pre><code>
network_data = {
  "nodes": ["U", "V", "W", "X", "Y", "Z"],
  "edges": [
    {"source": "U", "destination": "V", "cost": 2},
    {"source": "U", "destination": "X", "cost": 1},
    {"source": "U", "destination": "W", "cost": 5},
    {"source": "V", "destination": "W", "cost": 3},
    {"source": "V", "destination": "X", "cost": 2},
    {"source": "X", "destination": "W", "cost": 3},
    {"source": "X", "destination": "Y", "cost": 1},
    {"source": "W", "destination": "Y", "cost": 1},
    {"source": "W", "destination": "Z", "cost": 5},
    {"source": "Y", "destination": "Z", "cost": 2}
  ],
  "start_node": "U"
}
</code></pre>

<p align="center">
  <img src="/images/InitialGraphExample.png" alt="Generated graph with JSON definition" width="500">
  <br>
  Graph initialization after indicating the number of nodes
</p>

Automagtic generation and visualization of Graph, including Nodes, Connections and Costs associated to each.

### Manual graph definition
Graph can be generated manually following the JSON format previously shown. 

1. Create a new code cell.
2. Generate the new graph with name "network_data".
3. Do not execute "Generation of a network" to avoid overwriting the created graph.
4. Execute "Computation of Dijkstra" code cell

### Automatic graph definition
A random graph can be generated automatically using the "Generation of a network" code cell

#### Step 1
Define the number of nodes with the slider and press "Generate Graph" to generate the graph. 

>[!NOTE]
> The connections and costs are randomly generated
>
<p align="center">
  <img src="/images/GraphGen01.png" alt="Graph Initialization" width="600">
  <br>
  Graph initialization after indicating the number of nodes
</p>

#### Step 2
The program will show the graph once generated.

<p align="center">
  <img src="/images/GraphGen02.png" alt="Graph Initialization" width="500">
  <br>
  Graph visualization, including nodes, connections and costs
</p>

And, finally, requests for the origin node

<p align="center">
  <img src="/images/GraphGen03.png" alt="Graph Initialization">
  <br>
  Selection of initial node
</p>

> [!WARNING]  
> The "Process Dijkstra" button is stil not working. Manual execution of the code block is required once the graph is defined.


## Dijkstra minimum cost path computation

Based on classical Dijkstra minimum cost path algorithm for graphs. Shows, at each iteration, the graph status and table with minimum distances

At each step, the program shows the graph with the nodes and the table
<p align="center">
  <img src="/images/DJKStep01.png" alt="Example of algorithm iteration">
  <br>
  Example of algorithm iteration. Green nodes: Already in N', Blue nodes: Nodes in study (connected with current node)
</p>  

At each step, the program shows the graph with the nodes and the table
<p align="center">
  <img src="/images/DJKStep01.png" alt="Example of algorithm iteration">
  <br>
  Example of algorithm iteration. Green nodes: Already in N', Blue nodes: Nodes in study (connected with current node)
</p>  

At each step, the program shows the graph with the nodes and the table
<p align="center">
  <img src="/images/DJKStep01.png" alt="Example of algorithm iteration">
  <br>
  Example of algorithm iteration. Green nodes: Already in N', Blue nodes: Nodes in study (connected with current node)
</p>  

At the end of the computation, it shows the resulting tables with the computation

<p align="center">
  <img src="/images/DJKStepFinal.png" alt="Final results">
  <br>
  Selection of initial node
</p>  


## Dijkstra minimum cost paths animated sequence

Last code cell creates a sequence of resulting minimum cost paths including:

* Paths to destination node
* Partial costs
* Total cost
* Graphical representation of the path inside the graph (red lines)

Use the reproduction buttons to execute the animation.

<p align="center">
  <img src="/images/DJKStepAnimation.png" alt="Final results">
  <br>
  Selection of initial node
</p>  

