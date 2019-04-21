# Process Lineage - see the dependency graph using NetworkX

Every complex data processing environment consists of hundreds of data pipelines. Each of these pipelines is called a workflow. A workflow may have several steps to move data around. Every unit of work within a workflow is referred as task. These tasks have dependency among them. Tasks within a workflow along-with their dependencies can be viewed as a directed acyclic graph (DAG).

Following is a task dependency graph of a workflow  DAG drawn using [DOT language](https://www.graphviz.org/doc/info/lang.html)

<img src="images/first_sample.dot.svg">

Workflows have dependency across them. Specifically a task in a workflow can depend on a predecessor task in the same workflow or on a task in different workflow. Next diagram shows such a scenario. Here also the diagram is generated using DOT language and using clustering of nodes to contrast one workflow from another.

<img src="images/second_sample.dot.svg">


### References

* [DOT language](https://www.graphviz.org/doc/info/lang.html)
* [Drawing graphs with dots](https://www.graphviz.org/pdf/dotguide.pdf)


## Authors

* **Abhijit Bhattacharya** 
