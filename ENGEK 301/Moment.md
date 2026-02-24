The moment of something is distance times something. So, the moment of force, or torque, is a moment because it's distance times force. Meanwhile moment of inertia is the mass times the distance which is used to find center of mass. 
$$\vec M_A=\vec r_A\times\vec F_A$$
The angular velocity vector points on the axis of rotation, just as there are two ways to describe rotation, there are also two ways of expressing the axis (an infinite pole) via a sign.

A rotation is a matrix, so the time derivative of rotation is supposed to be a matrix as well. But it's a vector posing as an anti-symmetric matrix. But that's too much to handle for some reason.

When you extend the line of force given a moment of force, the closest distance between the axis of rotation and the "line of action" is $L\sin\alpha$. So multiplying the two gets you:
$$\vec M_A=rF\sin\alpha$$
```
scratch:
r = 3cos30 i + 3sin30 j
F = 5cos45 i - 5cos45 j

-(15cos30cos45 - 15cos45sin30)k

r = 3 i
F = 5sin15 i - 5cos15 j

M = -15 q6 + q2/4 k = 14.5

r_s = 3sin75
F = 5 kN

same result.

+4 +2 -1
-2 +6 +3

(12 -10 28)
    -8  6 / 10


```
### Couple Moment
A couple moment is generated when equal and opposite forces act on different places. This generates no net force but does make a moment of force to apply torque. They can be treated as their own individual parts when summing up for the total moment around a point:
$$M_Q=M_1+M_2+\vec r_{QA}\times \vec F_A+\dots$$
You can also translate between points using the resultant force and a moment at a point:
$$M_P=M_Q+\vec r_{PQ}\times(\vec F_A+\dots)$$
### (Statically) Equivalent (Sets of) Force
Two sets of forces and moments are statically equivalent if they have the same resultant force and resultant moment about one point.