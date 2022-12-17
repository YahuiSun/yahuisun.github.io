---
layout: archive
title: ""
permalink: /rucgraph/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<a href="https://github.com/rucdatascience/rucgraph" target="_blank" rel="nofollow">rucgraph</a> is an open-source, easy-to-use library of cpp header files, mainly designed for performing graph computing tasks. It is on Github, and accepts Pull Requests! 


It contains different types of adjacency lists to represent a graph, e.g., "graph_v_of_v_idealID" is a simple adjacency list built using vectors, while "graph_hash_of_mixed_weighted" is a complex adjacency list built using a "dynamic" mixup of vectors and hashes. It is easy to uses these adjacency lists. For example, the followings codes first build a graph with 5 vertices and 2 edges, and then print 3 components of this graph.
```
        graph_v_of_v_idealID g(5); // a graph with 5 vertices: 0, 1, 2, 3, 4, 5
	graph_v_of_v_idealID_add_edge(g, 0, 1, 0.3); // add edge (0,1) with the weight of 0.3 
	graph_v_of_v_idealID_add_edge(g, 3, 4, 0.5); // add edge (1,2) with the weight of 0.5
	std::list<std::list<int>> cpns = graph_v_of_v_idealID_connected_components(g); // find the connected components of g
	for (auto it = cpns.begin(); it != cpns.end(); it++) {
		print_a_sequence_of_elements(*it);
	}
```



