# Ex.No: 2  Implementation of Depth First Search
### DATE: 17-02-2024                                                                            
### REGISTER NUMBER : 212221060113
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:
```
def dfs(graph, node, visited):
    if node not in visited:
        print(node, end=' ')
        visited.add(node)
        if node in graph:
            for neighbor in graph[node]:
                dfs(graph, neighbor, visited)

# Given partial graph
graph = {
    '1': ['2', '3'],
    '2': ['4', '5'],
    '3': ['6', '7'],
}

# Set to keep track of visited nodes
visited = set()

# Perform DFS traversal starting from each node if not visited
print("DFS traversal starting from each node:")
for node in graph:
    dfs(graph, node, visited)
```

### Output:

![image](https://github.com/Chandru0021/AI_Lab_2023-24/assets/131637082/8589dea6-a1df-42fc-81e5-d196f345534c)


### Result:
Thus the depth first search order was found sucessfully.
