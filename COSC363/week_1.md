# grading
- Assignment 1 **20%**
- Assignment 2 **20%**
- Quizzes      **10%**
- Final Exam   **50%**

quizzes are open for 2 weeks, one attempt with penalty system.

# structure
main groups of content
- opengl 2
- ray tracing (oop incl) 
- opengl 4 (shaders)

# Objectives
- Graphics Theory
- Graphics Programming
- Methods/Algos

# Why are we using OpenGL

alternatives like vulkan are very useful but they expect a deeper understanding in computer graphics. So opengl is better for students.

opengl 1.0 and 2.0 are pretty simple, we can start with them and build up to opengl 4.0. Once again, useful for students.

# General structure of an OpenGl program

**core libraries**
- OpenGl
- GLU (OpenGL Utility Library) : high level funcs for viewing
- GLUT (OpenGl Utility Toolkit) : mainly used for event processing (interactivity)

### GLUT Built-in Objects
| name          | verticies         | faces
|:-             |:-                 |:-
| sphere        | *n/a*             | *n/a*
| torus         | *n/a*             | *n/a*
| cone          | *n/a*             | *n/a*
| teapot        | *n/a*             | *n/a*
| tetahedron    | 4                 | 4
| cube          | 8                 | 6
| octahedron    | 6                 | 8
| docecahedron  | 20                | 12
| icosadehron   | 12                | 20

## Basic OpenGl Program
### #include <GL/freeglut.h>
### void display(void) 
**this is a usr defined function** that is callbacked (called every time) OpenGL needs to refresh the display. We have to pass this function pointer for the callback functionality, (look at the main func)

| code | purpose | options
|:-|:-|:-
| ` float light[4] | define a inf light source point |
| ` glClear `      | clear buffers | using bitmasks
| ` glMatrixMode   |  setting the coordinate mode | 
| ` glLoadIdentity | |
| ` gluLookAt `    | sets the camera position and projection plane
| ` glLightfv `    | setting up light | 
| ` glColor3f `    | using single material color | 
| ` gluSolidTeapot | a GLUT built in object | 
| ` glFlush `      | empties buffers 


### void initialize(void) 
**this is a user defined function** it is ususally called inside of main

some examples of this function:
- enable some lighting (lights)
- background color
- camera is setup

| code                               | purpose                       | options
|:-                                  |:-                             |:-
| ` glClearColor(A,B,C,D); ` | set background color  | A B C D , RGBA? *not 100% sure yet*
| ` glEnable(A) ` | used to enable certian components in the scene | GL\_LIGHTING, GL\_LIGHT0, GL\_COLOR\_MATERIAL etc  
| ` `     


### int main()

| code                               | purpose                       | options
|:-                                  |:-                             |:-
| ` glutInit(&argc, argv); `         | needs to be called to init GLUT  |
| ` glutInitDisplayMode(A\|B); `     | init display buffer option    | `GLUT_SINGLE`=*single\_buffer* \| `GLUT_DEPTH`=*double\_buffer*
| ` glutInitWindowSize(A, B); `      | display window size           | *height*, *width*   
| ` glutInitWindowPosition(A, B); `  | init window position          | *ypos*, *xpos*
| ` initalize(); `                   | usr defined inits             | 
| ` glDisplayFunc(A); `              | display callback function     | function to callback to
| ` glMainLoop(); `                  | begins gl main looping        | infinite loop (**no code afterwards will be executed**)



# 3-D Scenes
3-D scenes generally include:
- serveral models
- uses complex transformations
- employs advanced rendering algorithms
- implements several animation sequences

# Render pipeline basics

![alt text](https://www.enlightenment.org/_media/playground/evasgl-graphics-pipeline.png)

## Primatives
- are basic polygonal shapes used for constructing 3D models
- primitive is defined using an ordered list of verticies
    - Trangles (3 v)
    - Quads (4 v)

### Front-Back Ambuguity
primatives do not have any information for faces, only boundry ponts. So:

- the **normal vector** represets the front face of a polygon. This vector is used for lighting calculations
- The verticies are usually **ordered in the anti-clockwise sense** with respect to the outward normal direction
- The normal is ultimatley used for rendering, and so it **also defines the orentation** of the primative.

# Coordinate Frame
3D points(xyz) and vectors are always defined in a **right handed** coordinate reference frame

![alt text](https://www.researchgate.net/publication/2457107/figure/fig1/AS:669571027595268@1536649581208/Right-and-Left-Handed-Coordinate-systems.png)


# Points and vectors
## Points
used for
- Defniing verticies of primitives
- positions of light sources
- camera position and orentation

## vector
used for
- specifying transformations
- directional light
- spotlight direction
- normal vectors
- ect

## homogenous Coordinates
we use **homogenous coordinates

# tips
- always think of openGL as a **state machine**
- **callbacks** are used to link events to usr code
- pretty much everything will be a **4x4 matrix** 




