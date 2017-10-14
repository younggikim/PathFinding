﻿# PathFinding
 introduces several path finding algorithms such as A*, Dijkstra, BFS and DFS ( Work in Progress )
# Examples
```
// returns pathway of directions and distance from start to end node.
// returns empty pathway and -1 of distance if no path found.

int distance;
List<Direction> pathWay = PathFinding.Search4WayNodeByAstar( startNode, (IMovable)endNode, this, out distance );

// returns pathway of directions from start and distance when ISearch interface decides it reaches a goal.
List<Direction> pathWay = PathFinding.Search4WayNodeByBFS( currentNode, (ISearch)this, (IMovable)this, out distance );
```
 
```
You should implement a class that has iterfaces of IMovable( for getting adjacent nodes ) and ISearch ( to know goal check ).
public interface IMovable
{
    bool IsMovableNode( Node pos );
}

public interface ISearch
{
    bool IsReachedDestination( Node Pos );
}
```
