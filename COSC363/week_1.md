# Week 1

### grading
- Assignment 1 **20%**
- Assignment 2 **20%**
- Quizzes      **10%**
- Final Exam   **50%**

quizzes are open for 2 weeks, one attempt with penalty system.

### structure
main groups of content
- opengl 2
- ray tracing (oop incl) 
- opengl 4 (shaders)

### Objectives
- Graphics Theory
- Graphics Programming
- Methods/Algos

## Why are we using OpenGL

alternatives like vulkan are very useful but they expect a deeper understanding in computer graphics. So opengl is better for students.

opengl 1.0 and 2.0 are pretty simple, we can start with them and build up to opengl 4.0. Once again, useful for students.

## General structure of an OpenGl program

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

### Basic OpenGl Program
#### #include <GL/freeglut.h>
#### void display(void) {
all display models
#### void initialize(void) {
parameter/state initialization
#### int main()

| code                               | purpose                       | options
|:-                                  |:-                             |:-
| ` glutInit(&argc, argv); `         | general purpose init          |
| ` glutInitDisplayMode(A\|B); `     | init display buffer option    | `GLUT_SINGLE`=*single\_buffer* \| `GLUT_DEPTH`=*double\_buffer*
| ` glutInitWindowSize(A, B); `      | display window size           | *height*, *width*   
| ` glutInitWindowPosition(A, B); `  | init window position          | *ypos*, *xpos*
| ` initalize(); `                   | usr defined inits             |
| ` glDisplayFunc(A); `              | display callback function     | function to callback to
| ` glMainLoop(); `                  | begins gl main looping        |
