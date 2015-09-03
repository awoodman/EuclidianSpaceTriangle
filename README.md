## CSCI 2312: Programming Assignment 1

_ADAM WOODMAN - PA1_

* * *

Introduction: 

My program asks the user to enter the coordinated in 3D space for three separate points, in the follwing way:

1) Asks user to enter x-coordinate for point 1
2) Asks user to enter y-coordinate for point 1
3) Asks user to enter z-coordinate for point 1
4) Asks user to enter x-coordinate for point 2
5) Asks user to enter y-coordinate for point 2
6) Asks user to enter z-coordinate for point 2
7) Asks user to enter x-coordinate for point 3
8) Asks user to enter y-coordinate for point 3
9) Asks user to enter z-coordinate for point 3

There are only three variables to store x,y, and z, for ALL three points, rather than 9, so it was necessary to call the constructors for
the point class, between #'s 3 and 4, and #'s 6 and 7, above.  To do this, I called a custom constructor that takes 
in three arguments (double xin, double yin, double zin) and sets those as the x, y, and z coordinates of the first, 
second, and then third point (called a, b, and c).

Once all of the coordinates are set the the user's input values, we can move on to how the program calculates the 
area of the triangle inscribed by these three points.  Heron's formula is used to calcualte the area of a triangle
in 3d space, and Heron's formula looks like area = sqrt(s*(s-side1)*(s-side2)*(s-side3)), where s is the perimeter 
of the triangle and Side1,2, and 3 are the lengths of the three sides on the triangle.  To find the side length, a
member function was added to the point class, called distanceTo.  This returns a double and accepts one argument,
which is a reference to a Point class.

When the function is called, like a.distanceTo(b), we are able to find the distance by accessing the x,y, and z coo-
rdinates of a and calculating the distnace between a and b by using getX(),getY(), and getZ() member functions and
some simple trigonometry.  Once we call the distanceTo function 3 times, we're able to calcualte 's', and finally, 
the area of the triangle.

The only thing the user see's is the prompts to enter the 9 coordinates and the line "The area of the triangle is: 123.45"
