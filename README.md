Download Link: https://assignmentchef.com/product/solved-cosc6000-homework11
<br>



ProjectileMain.cpp

Projectile.h Projectile.cpp vector2d.h vector2d.cpp from Canvas site: <strong><u>Link</u></strong>

Create a project on your IDE (Xcode, Visual Studio)

For Visual Studio, it may be better to create, ‘vector2d’ and ‘Projectile’ class and copy and paste the codes.

This code solves the projectile of an object within frictionless fluid.

The governing equation is:

is the gravitational acceleration, which is:

<h2>Compu ng the velocity Since</h2>

the finite difference form of above equation (first order Euler method) is Therefore the update scheme for the velocity with in a time step,   is:

<h2>Compu ng the posi on coordinate</h2>

the finite difference form of above equation (first order Euler method) is

Therefore the update scheme for the position coordinate with in a time step,   is:

<h2>Analy cal Solu on</h2>

The governing equation can be solved analytically. where

<h1>Assignment</h1>

We want to develop a code to simulate the projectile of a ball/bullet in a viscous fluid. The trajectory of the ball/bullet can be described by three components; the coordinate , the velocity  and the acceleration

.

The governing equation is:

is the gravitational acceleration, D is a drag coefficient.

Develop the class “<strong>ProjectileWithDrag</strong>” that will provide a method to compute the trajectory of an object in a viscous fluid with a non­linear drag.

Define the class “<strong>ProjectileWithDrag</strong>” <u>derived from “<strong>Pro</strong></u><strong>j<u>ectile</u></strong><u>”</u> class.

a constructor that takes the bullet <strong>weight</strong>, the bullet <strong>initial speed</strong> , <strong>the angle</strong>, and <strong>the drag coefficien</strong>t, D.

set the initial velocity using <strong>the initial speed</strong> and <strong>the angle</strong>.

set the initial coordinate to (0,0), acceleration to (0,­g), and the time to 0. a default constructor (takes no input) that initialize all member variable to zero. Redefine <strong>update(double dt)</strong> that updates the coordinate, velocity and acceleration as

Modify the main function to test your class.

Try making a plot of your result and compare with the drag­free case.