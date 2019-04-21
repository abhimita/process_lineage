# Process Lineage - see the dependency graph using NetworkX

Every complex data processing environment consists of hundreds of data pipelines. Each of these pipelines is called a workflow. A workflow may have several steps to move data around. Every unit of work within a workflow is referred as task. These tasks have dependency among them. Tasks within a workflow along-with their dependencies can be viewed as a directed acyclic graph (DAG).

Following is a task dependency graph of a workflow  DAG drawn using [DOT language](https://www.graphviz.org/doc/info/lang.html)

<img src="images/first_sample.dot.svg">

Workflows have dependency across them. Specifically a task in a workflow can depend on a predecessor task in the same workflow or on a task in different workflow. Next diagram shows such a scenario. Here also the diagram is generated using DOT language and using clustering of nodes to contrast one workflow from another.

<img src="images/second_sample.dot.svg">

# Problem statement

Most of the industry grade orchestration tool like [Airflow](https://airflow.apache.org/) or [Azkaban](https://azkaban.github.io/) provide polished UI to look at intra and inter-workflow dependency though dependency across multiple workflows may require multiple navigational action (mouse clicks) and it becomes challenging to remember context after navigating multiple levels. But this is not the main problem statement. 

Now each of the tasks in workflow has several attributes. For example - run time, start time etc. Attributes like run time can vary from one day to another as the volume of data processed can change from one day to another. To keep things simple, I will assume run time is not varying - let us assume that we are dealing with median value of the run time of each task if we have access to historical task & workflow run time data. 

### References

* [DOT language](https://www.graphviz.org/doc/info/lang.html)
* [Drawing graphs with dots](https://www.graphviz.org/pdf/dotguide.pdf)


## Authors

* **Abhijit Bhattacharya** 
