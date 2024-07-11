# SuccessiveConvexification
Implementation of [Successive Convexification: A Superlinearly Convergent Algorithm for Non-convex Optimal Control Problems
](https://arxiv.org/abs/1804.06539) by Yuanqi Mao, Michael Szmuk and Behcet Acikmese

Reqires `matplotlib`, `numpy`, `scipy` and `cvxpy`.

This framework provides an easy way to implement your own models.

Fixed- and free-final-time optimization is possible.

The following models are currently implemented:

- Differential drive robot path planning with free-final-time and non-convex obstacle constraints:
![](https://i.imgur.com/xNaD5eP.png)

v2.1 To prevent empty spaces between obstacles, I segmented the track based on its length when adding obstacles. But it still has a problem:
![problem01.png](output%2Fproblem01.png)

v2.1.1 I want to minimize the length of trajectory, by adding the length in objectives.

v2.2 To prevent such problem, X is initialized to the center of the track.

v2.3 Add constrain about acceleration.

v2.4 Plotting initial trajectory.