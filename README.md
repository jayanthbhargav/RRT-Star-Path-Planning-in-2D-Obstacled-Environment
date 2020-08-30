# RRT-Star-Path-Planning-in-2D-Obstacled-Environment

The steering function for the RRT* algorithm takes a given start and destination point and
gives the optimal path. Here, the control input is constrained between -1 and 1 and the requirement is
to reach the goal as fast as possible. The given system dynamics is a first order system where the
control input is the velocity of the robot. Assuming that we can apply the maximum allowable input
( u = 1) at all steps of the path, we can argue that the shortest distance path will be the most optimal
path. Therefore, the cost function for the algorithm in this case would be the distance itself.

o Sample Function: Samples a point in the obstacle free space

o Steer Function: Finds a point in the neighborhood to the nearest node in the tree along the line
joining the new node and nearest node.

o Connect Function: Connects the new node the tree with the parent as the nearest node. After
this is done, the rewire function will rewire this new node if it can get a better parent

o Rewire Function: This function rewires all the points around a node within a ball of radius (r)
to better parents (in the sense of cost)
