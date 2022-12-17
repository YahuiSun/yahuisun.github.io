---
layout: archive
title: ""
permalink: /rucgraph/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# A brief introduction

I am maintaining an open-source, easy-to-use library of cpp header files: <a href="https://github.com/rucdatascience/rucgraph" target="_blank" rel="nofollow">rucgraph</a>, which is mainly designed for performing graph computing tasks. It accepts Pull Requests on Github! 
<p align="center">
<img src="/_pages/assets/20221217211817.png" alt="drawing" width="400"/>
</p>

It contains different types of adjacency lists to represent a graph, such as a simple adjacency list built using vectors, as well as a complex adjacency list built using a "dynamic" mixup of vectors and hashes. 
It is easy to uses these adjacency lists. For example, the following codes first build a graph with 5 vertices and 2 edges, and then find and print 3 components of this graph.
```
graph_v_of_v_idealID g(5); // a graph with 5 vertices: 0, 1, 2, 3, 4, 5
graph_v_of_v_idealID_add_edge(g, 0, 1, 0.3); // add edge (0,1) with the weight of 0.3 
graph_v_of_v_idealID_add_edge(g, 3, 4, 0.5); // add edge (1,2) with the weight of 0.5
auto cpns = graph_v_of_v_idealID_connected_components(g); // find the connected components of g
for (auto it = cpns.begin(); it != cpns.end(); it++) 
{
	print_a_sequence_of_elements(*it);
}
	
/*
Printing results:
0 1 // 1st component
2   // 2nd component
3 4 // 3rd component
*/
```

<br/>

# Highlights

## A Pairing Heap that can change all keys in O(1) time

rucgraph contains <span style="color:red">an augmented Pairing Heap that can change all keys in O(1) time!</span> It achieves this by associating an offset value with each node in the heap. To use this heap, include the following header file in your codes.
```
#include <data_structures/PairingHeapYS_with_offset.h>
```



