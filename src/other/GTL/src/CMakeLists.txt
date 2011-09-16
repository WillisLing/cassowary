include_directories(
	${CMAKE_CURRENT_SOURCE_DIR}/../include
	${CMAKE_CURRENT_BINARY_DIR}/../include
	)

SET(gtl_srcs
	bellman_ford.cpp
	bfs.cpp
	biconnectivity.cpp
	bid_dijkstra.cpp
	components.cpp
	debug.cpp
	dfs.cpp
	dijkstra.cpp
	embedding.cpp
	fm_partition.cpp
	maxflow_ff.cpp
	maxflow_pp.cpp
	maxflow_sap.cpp
	min_tree.cpp
	planarity.cpp
	pq_node.cpp
	pq_tree.cpp
	ratio_cut_partition.cpp
	st_number.cpp
	topsort.cpp
	edge.cpp
	gml_parser.cpp
	gml_scanner.cpp
	graph.cpp
	node.cpp
	)

add_library(gtl SHARED ${gtl_srcs})
SET_TARGET_PROPERTIES(gtl PROPERTIES VERSION ${GTL_SO_VERSION} SOVERSION ${GTL_LIB_CURRENT})
