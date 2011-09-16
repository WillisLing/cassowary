SET(pkginclude_HEADERS =
	GTL.h
	algorithm.h
	bfs.h
	biconnectivity.h
	debug.h
	dfs.h
	edge.h
	edge_data.h
	edge_map.h
	embedding.h
	gml_parser.h
	gml_scanner.h
	graph.h
	ne_map.h
	node.h
	node_data.h
	node_map.h
	planarity.h
	pq_node.h
	pq_tree.h
	st_number.h
	symlist.h
	topsort.h
	maxflow_ff.h
	maxflow_pp.h
	maxflow_sap.h
	components.h
	fm_partition.h
	ratio_cut_partition.h
	min_tree.h
	dijkstra.h
	bellman_ford.h
	bin_heap.h
	bid_dijkstra.h
	)

configure_file(${CMAKE_CURRENT_SOURCE_DIR}/version.h.in ${CMAKE_CURRENT_BINARY_DIR}/version.h @ONLY)
