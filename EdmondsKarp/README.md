## Edmonds & Karp
### Input :
<ul>
    <li>adjacency matrix</li>
    <li>source</li>
    <li>sink</li>
</ul>

### Output : 
<ul><li>maximum flow</li></ul>

### Algorithm : 
```
EdmondsKarp(adjMatrix, source, sink)
    resCapArray <-- [] 
    while(path != NULL)
        flow <-- min(foreach (u, v) in path adjMatrix[u][v] - resCapArray[u][v])
        foreach (u, v) in path
            update resCapArray
    return sum(every flow passing through)
```

### CSV file format (only the values)
|        | Node 1 | Node 2 | Node 3 | Node 4 | Node 5 |
|:------:|:------:|:------:|:------:|:------:|:------:|
| Node 1 |0       |    ?   |?       |?       |?       |
| Node 2 |    ?   |   0    |       ?|     ?  |?       |
| Node 3 |    ?   |    ?   |   0    |     ?  |?       |
| Node 4 |    ?   |    ?   |     ?  |   0    |?       |
| Node 5 |    ?   |    ?   |      ? |    ?   |  0     |