# D3bie

Simple D3 practice codes


# Example:

- [AddElement-DataBinding](https://hasanmansur.github.io/D3bie/AddElement-DataBinding.html)
- [DrawingDivs](https://hasanmansur.github.io/D3bie/DrawingDivs.html)
- [DrawingSVG](https://hasanmansur.github.io/D3bie/DrawingSVG.html)
- [BarChart](https://hasanmansur.github.io/D3bie/BarChart.html)
- [Scatterplot](https://hasanmansur.github.io/D3bie/Scatterplot.html)
- [ForceDirectedGraph(NonDraggable)](https://hasanmansur.github.io/D3bie/ForceDirectedGraphNonDraggable.html)
- [ForceDirectedGraph(Draggable)](https://hasanmansur.github.io/D3bie/ForceDirectedGraphDraggable.html)
- [LineChart](https://hasanmansur.github.io/D3bie/linechart.html)

# Some Notes on Force Directed Graph

* A simulation created for an array of nodes, and desired forces are composed on it. Then tick events are listened to render the nodes with modified positions.

* Each node must be an object. The following properties are assigned by the simulation:
  > index - the node’s zero-based index into nodes
  > x - the node’s current x-position,
  > y - the node’s current y-position,
  > vx - the node’s current x-velocity,
  > vy - the node’s current y-velocity

* To fix a node in a given position, you may specify two additional properties:
  > fx - the node’s fixed x-position,
  > fy - the node’s fixed y-position

* At the end of each tick, after the application of any forces, a node with a defined node.fx has node.x reset to this value and node.vx set to zero; likewise, a node with a defined node.fy has node.y reset to this value and node.vy set to zero. To unfix a node that was previously fixed, set node.fx and node.fy to null, or delete these properties.

* Simulations typically compose multiple forces as desired. Some are as follows:
- The centering force translates nodes uniformly so that the mean position of all nodes is at the given position ⟨x,y⟩.
- The link force pushes linked nodes together or apart according to the desired link distance.
- The many-body (or n-body) force applies mutually amongst all nodes. It can be used to simulate gravity (attraction) if the strength is positive, or electrostatic charge (repulsion) if the strength is negative. 
