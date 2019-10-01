# Investigating Connectedness of Cities’ Transportation Networks
## Abstract
In this project, we want to examine multilayer graphs that model transportation networks in cities. Primarily, we want to understand how adding additional connections both within layers and between layers can increase the connectedness of graph, and how increased connections could decrease the commute time between random nodes of the graph. We will investigate different methods of adding connections for a variety of different city types (car dominated, bike dominated, metro dominated, etc). The primary goal is to understand how modern cities can improve their transportation networks, and how bike networks in particular can be shown to be cost effective methods of improving the commutability of cities.

## Bibliography and Inspiration
Luis Guillermo Natera Orozco1 , Federico Battiston1 , Gerardo Iñiguez1,2,3 , Michael Szell4,5*
https://arxiv.org/abs/1907.07080
The authors model cities as multiplex transport networks, basically undirected graphs that have multiple layers that can have different degrees of connectedness between the layers. They set out to find the best way to optimize a city to accommodate bicycles. The different layers are the different networks for transportation: a bicycle network, car network, subway network, etc. The goal is to find the connectedness between the different layers and the disconnectedness of the bicycle network and find the most optimal way to grow the bicycle network such that it has the most connected parts. They use several algorithms for connecting the fragments of the network. The first one connects the largest fragment to the second largest fragment. The next method was connecting the largest fragment to the closest fragment to that largest fragment. They predominately used the Largest to Closest algorithm and rank each city on how will it performs given a certain number of kilometers it can extend the bicycle network to create the most connected network.  

## Proposed Experiments
* Recreate experiments carried out in the paper, namely:
  * Connect sections of the graph based on size
  * Connect sections of the graph based on proximity
* Extensions:
  * Define a commute time per unit length of transportation method (between two randomly chosen points) and see how commute time changes as a function of length of transportation paths added
  * Define a cost per unit length for each transportation method, and for a given budget, see which method of transportation decreases commute time the most

## Potential Graphs
![graph](https://github.com/jzerez/ComplexityScienceProject1/blob/master/reports/assets/potential_graph.PNG)

## Expected Results
* If we plotted the average commute vs the average length of the path added per step we might expect to see a sigmoid-like graph where there is a turning point of  optimal way to add paths (adding more short paths vs fewer long paths)
  * If this is the case we would look for the equivalent of the p value from the w-s graphs
* We think the overall sizes of the graphs will be pretty similar so large scaling won’t really be looked into

## Potential Concerns
* Implementing multi-layer graphs seems difficult
* Reconciling dimensionality of nodes. (ie: shortest path length between two nodes graphically is not the same as the shortest path length between two physical locations)
* Generating/quantifying ‘realistic’ graphs
* There are a lot of directions that we could go with this, and determining more specifically what we want to accomplish will be important

## Next Steps
* Get access to the data they used for their networks
* Make scaled-down models for testing
  * 50-100 node fragmented graphs
  * Arrange graph based on distances, make it look like a city
  * Try to implement some fragment-connecting algorithms
  * Make graph analysis algorithms - path length, connectedness, can you get from path a to b
