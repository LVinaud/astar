# The Algorithm

Let's consider a square grid, in which each node is either a unavailable point, a possible path, the destination or the origin.

The destination location is known.

A priority queue is needed in order to always check for the lower cost next node. (The cost of a node is simply its distance to the origin,
calculated by the sum of the distances up until there, plus it's euclidian distance to the destination)

If a dijkstra method is wanted, one must simply deduct this euclidian distance, as in only caring for the current distance travelled.

Starting with the origin we check if the node being analyzed is the destination and if not, the possible paths in adjacency are added to
the priority queue. The loop continues until the queue is empty or the destination is found. To reacreate the path the previous square 
for each node is stored in a matrix.
