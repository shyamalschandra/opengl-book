#OpenGL 2.1 Bible (Rough Cuts Preliminary Version)

##Author: Shyamal Chandra
###Date: January 20, 2017

#####How do you begin drawing a complex shape in OpenGL?

####C syntax:

`void glBegin(GLenum mode);`

mode: ""Specifies the primitive or primitives that will be created from vertices presented between glBegin and the subsequent glEnd. Ten symbolic constants are accepted: GL_POINTS, GL_LINES, GL_LINE_STRIP, GL_LINE_LOOP, GL_TRIANGLES, GL_TRIANGLE_STRIP, GL_TRIANGLE_FAN, GL_QUADS, GL_QUAD_STRIP, and GL_POLYGON."" [1]

#####How do you end drawing a complex shape in OpenGL?

####C syntax:

`void glEnd(void);`

#####How do you specify a point mode in OpenGL inside a `glBegin()` call?

####C syntax:

`GL_POINTS`

""Draws points on screen. Every vertex specified is a point."" [2]

`GL_LINES`

""Draws lines on screen. Every two vertices specified compose a line."" [2]

`GL_LINE_STRIP`

""Draws connected lines on screen. Every vertex specified after first two are connected."" [2]

`GL_LINE_LOOP`

""Draws connected lines on screen. The last vertex specified is connected to first vertex."" [2]

`GL_TRIANGLES`

""Draws triangles on screen.  The last vertex specified compose a triangle."" [2]

`GL_TRIANGLE_STRIP`

""Draws connected triangles on screen. Every vertex specified after first three vertices creates a triangle."" [2]

`GL_TRIANGLE_FAN`

""Draws connected triangles like GL_TRIANGLE_STRIP, except draws triangles in fan shape."" [2]

`GL_QUADS`

""Draws quadrilaterals (4 – sided shapes) on screen. Every four vertices specified compose a quadrilateral."" [2]

`GL_QUAD_STRIP`

""Draws connected quadrilaterals on screen. Every two vertices specified after first four compose a connected quadrilateral.""

`GL_POLYGON`

""Draws a polygon on screen. Polygon can be composed of as many sides as you want.""

####C snippet:

```
glBegin(GL_TRIANGLES);
	glVertex3f(0.0,0.0,-10.0);
	glVertex3f(1.0,0.0,-10.0);
	glVertex3f(0.0,1.0,-10.0);
glEnd();
```

#####How do you specify a vertex when drawing objects in two-dimensional space?

`void glVertex2s(	GLshort x, 	GLshort y)`
`void glVertex2i(	GLint x, 		GLint y);`
`void glVertex2f(	GLfloat x,	GLfloat y);`
`void glVertex2d(	GLdouble x,	GLdouble y);`
`void glVertex3s(	GLshort x,	GLshort y,	GLshort z);`
`void glVertex3i(	GLint x,		GLint y,	GLint z);`
`void glVertex3f(	GLfloat x,	GLfloat y,	GLfloat z);` 
`void glVertex3d(	GLdouble x,	GLdouble y,	GLdouble z);`
 `void glVertex4s(	GLshort x,	GLshort y,	GLshort z,	GLshort w);`
 `void glVertex4i(	GLint x,		GLint y,	GLint z,	GLint w);`
`void glVertex4f(	GLfloat x, GLfloat y, GLfloat z, GLfloat w);` 
`void glVertex4d(	GLdouble x,	GLdouble y,	GLdouble z,	GLdouble w);` [3]

#####How do you specify a set of points in two-dimensional space?

####C snippet:
```
glPointSize(10.0);

glBegin(GL_POINTS);
	glVertex3f(1.0,1.0,0.0)
	glVertex3f(-1.0,-1.0,0.0);
glEnd();
```

[1]: https://www.opengl.org/sdk/docs/man2/xhtml/glBegin.xml
[2]: https://en.wikibooks.org/wiki/OpenGL_Programming/GLStart/Tut3
[3]: https://www.opengl.org/sdk/docs/man2/xhtml/glVertex.xml
